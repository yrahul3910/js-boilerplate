# JavaScript Boilerplate
This boilerplate is taken from [Cory House's Pluralsight course](https://app.pluralsight.com/library/courses/javascript-development-environment/table-of-contents).

# Configurations
The following is the setup used in this boilerplate.

## EditorConfig
EditorConfig is the choice of editor configuration management. The settings in the file use spaces for indenting, and an indent size of 4.

## Vulnerability Checking
The boilerplate uses Node Security Platform to check for vulnerabilities. Run
```
sudo npm i -g nsp
nsp check
```
to check for vulnerabilities manually.

## Dev Server
Express is the choice of dev server, though there are alternatives:
* Budo is useful if using Browserify as the bundler
* Webpack Dev Server is useful when using Webpack for bundling
* BrowserSync is helpful for cross-browser testing, supporting synced interactions

## Sharing Work-in-Progress
Localtunnel is used to share work. Alternatives are
* ngrok also allows for secure tunneling
* Now uploads the work to a cloud provider to production.
To share work, start the Express server, and in another terminal, type
```
lt --port 9000 --subdomain <preferred subdomain>
```
BrowserSync works with Localtunnel as well.

## Automation Tool
NPM scripts are used in this boilerplate, but Gulp is a good alternative. `npm-run-all` is used to run tasks parallely.

## Transpiling
Babel is used for transpiling. TypeScript and Elm are other alternatives. To use React, add `"react"` to the `presets` array in `.babelrc`, and run
```
npm i --save-dev babel-preset-react eslint-plugin-react
```
Then add
```
"plugins: [
    "react"
]
```
to the `.eslintrc` file.

## Bundling
Webpack is used over Browserify.

## Linting
An ESLint config file, `.eslintrc`, has been provided. `eslint-watch` is used to monitor constantly.

## Testing
Mocha is used for automated unit testing. Jest is a framework by Facebook that's a wrapper around Jasmine, and is useful with React. Jest has assertion built in, but since Mocha doesn't, Chai is used for assertion.
JSDOM and Cheerio are the helper libraries used.  
