## Google I/O 2015 web app

### Setup

1. `git clone https://github.com/GoogleChrome/ioweb2015.git`
2. `cd ioweb2015/app`
3. `bower install`
4. `npm install`

If you plan on modifying source code, be a good citizen and:

1. Install [EditorConfig plugin](http://editorconfig.org/#download) for your favourite browser.
   The plugin should automatically pick up the [.editorconfig](.editorconfig) settings.
2. Add pre-commit git hook:
   ```
   cp .git-hooks/pre-commit .git/hooks && chmod +x .git/hooks/pre-commit
   ```

   This will check for JS errors and code style before committing to the `master` branch.

### Running

Start a web server in `app/` or server via App Engine dev server.

**Note**: You have to run `gulp` or `gulp compass` at least once to generate CSS from the .scss files.

### Building

Run `gulp`. Then hit `http://localhost:<PORT>/dist/app/`. The unbuilt version is still viewable at `http://localhost:<PORT>/app/` but will not contain minfied JS or vulcanized HTML Imports.

**Note**: Build won't succeed if either `gulp jshint` or `gulp jscs` reports errors.
