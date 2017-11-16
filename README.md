# aurelia-cli-app

1. [Install Node.js](https://nodejs.org/en/)
1. [Install Git client](https://desktop.github.com/)
1. Configure npm proxies
```
npm config set proxy http://"{user name:url encoded password}"@proxy.us.dell.com:80
npm config set https-proxy http://"{user name:url encoded password}"@proxy.us.dell.com:80
```
1. Set user environment variables 
 - **HTTP_PROXY** with value `http://"{user name:url encoded password}"@proxy.us.dell.com:80`
 - **HTTPS_PROXY** with value `http://"{user name:url encoded password}"@proxy.us.dell.com:80`
1. Run command `npm install aurelia-cli`
1. Run command `au new`
1. Enter the following configuration selections accepting the default setting when applicable
```
Please enter a name for your new project below.

[aurelia-app]> aurelia-cli-app

Would you like to use the default setup or customize your choices?

1. Default ESNext (Default)
   A basic web-oriented setup with Babel and RequireJS for modern JavaScript development.
2. Default TypeScript
   A basic web-oriented setup with TypeScript and RequireJS for modern JavaScript development.
3. Custom
   Select loaders (requirejs/systemjs), bundlers (cli/webpack), transpilers, CSS pre-processors and more.

[Default ESNext]> 3

Which module loader / bundler would you like to use?

1. RequireJS (Default)
   A file and module loader for JavaScript.
2. SystemJS
   Dynamic ES module loader
3. Webpack
   A powerful bundler

[RequireJS]> 2

What transpiler would you like to use?

1. Babel (Default)
   An open source, standards-compliant ES2015 and ESNext transpiler.
2. TypeScript
   An open source, ESNext superset that adds optional strong typing.

[Babel]> 1

How would you like to setup your template?

1. Default (Default)
   No markup processing.
2. Minimum Minification
   Removes comments and whitespace between block level elements such as div, blockquote, p, header, footer
   ...etc
3. Maximum Minification
   Removes comments, script & link element [type] attributes and all whitespace between all elements. Also remove
   attribute quotes where possible. Collapses boolean attributes.

[Default]> 3

What css processor would you like to use?

1. None (Default)
   Use standard CSS with no pre-processor.
2. Less
   Extends the CSS language, adding features that allow variables, mixins, functions and many other
   techniques.
3. Sass
   A mature, stable, and powerful professional grade CSS extension.
4. Stylus
   Expressive, dynamic and robust CSS.
5. Post CSS
   A tool for transforming CSS with JavaScript.

[None]> 1

Would you like to configure unit testing?

1. Yes (Default)
   Configure your app with Jasmine and Karma.
2. No
   Skip testing. My code is always perfect anyway.

[Yes]> 1

What is your default code editor?

1. Visual Studio Code (Default)
   Code editing. Redefined. Free. Open source. Runs everywhere.
2. Atom
   A hackable text editor for the 21st Century.
3. Sublime
   A sophisticated text editor for code, markup and prose.
4. WebStorm
   A lightweight yet powerful IDE, perfectly equipped for complex client-side development.
5. None of the Above
   Do not configure any editor-specific options.

[Visual Studio Code]>

Project Configuration

    Name: aurelia-cli-app
    Platform: Web
    Bundler: Aurelia-CLI
    Loader: SystemJS
    Transpiler: Babel
    Markup Processor: Maximum Minification
    CSS Processor: None
    Unit Test Runner: Karma
    Editor: Visual Studio Code


Would you like to create this project?

1. Yes (Default)
   Creates the project structure based on your selections.
2. Restart
   Restarts the wizard, allowing you to make different selections.
3. Abort
   Aborts the new project wizard.

[Yes]>
Project structure created and configured.


Would you like to install the project dependencies?

1. Yes (Default)
   Installs all server, client and tooling dependencies needed to build the project.
2. No
   Completes the new project wizard without installing dependencies.

[Yes]>
```
1. Run the application `au run --watch`
 - The watch flag will keep the browser in sync with file changes in real-time

 ## PCF
 Deploying to PCF is simple using the Static File buildpack.

 A requirement of the buildpack is to include an empty Staticfile file in the root of the application.

 See the deploy.sandbox.bat and manifest.sandbox.yml files for commands and configurations

 - article about pushing on the production ready code to PCF... http://www.starkandwayne.com/blog/speed-up-the-staticfile-buildpack-only-deploy-the-dist-folder/
