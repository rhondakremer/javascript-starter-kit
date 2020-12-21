# Javascript Starter Kit

What should be in this starter kit?
* package management
* bundling
* minification
* sourcemaps
* transpiling
* dynamic html generation
* centralized http
* mock api framework
* component libraries
* development webserver
* linting
* automated testing
* continuous integration
* automated build
* automated deployment
* working example app

*********************************

## Editor Config
visit editorconfig.org to check if editor has built-in support, may need to download plugin

## Package Manager
there are more besides npm! Bower, JSPM, Jam, volo

## Development Web Server
six "interesting" options: http-server (super lightweight, no config, no live reloading), live-server, Express (production grade), budo, Webpack dev server (convenient if you're using webpack), Browsersync (dedicated IP! and different views will stay in sync)

Express is the only one listed that works for production

Express competitor: koa and hapi

sharing work in progress: localtunnel, ngroc, surge, now

## Automation
npm-run-all --parallel

## Transpiling
Babel, Typescript, Elm
Typescript: enhance autocomplete, enhanced readability, safer refactoring, additional non-standard features
Babel: write standard JS, leverage full JS ecosystem, use experimental features earlier, no type defs or annotations required, ES6 imports statically analyzable
Elm: compiles down to JS, clean syntax, immutable data structures, friendly errors, all errors are compile-time, can write with JS

Babel: two methods for configuration, .babelrc (not npm specific) or package.json

transpile for your environment

## Bundling
npm packages use CommonJS pattern... good for Node, doesn't work in browsers
Bundle npm packages into a format browsers can consume
may use bundlers to package js into one file, or portioned files... ie not just for browsers

5 module formats: 
1) IIFE 
2) Asynchronous Module Definition (AMD) 
3) CommonJS (CJS)
4) Universal Module Definition (UMD)
5) * ES6 Modules *

Why use ES6 Modules?
standardized, statically analyzable, named imports, default exports, easy to read

good options: browserify (the original), webpack (more than just js- css, images, html), rollup (first bundler to use tree shaking, faster loading production code), jspm (uses SystemJS, can load modules at runtime)

Webpack- bundle splitting so users don't have to load all js upfront
hot module reloading

## Testing & CI
Decisions!
### Framework
Mocha *
Jasmine- includes built-in assertion lib
Tape
QUnit
AVA
Jest

### Assertion Library
Chai popular but there are others

### Helper Libraries
JSDom- simulates DOM without using browser
Cheerio- jQuery for the server

### Where to run tests
browser- karma, testem
headless browser- phantomjs
in-memory DOM- JSDOM

### Where to place test files
folder called tests
### When to run tests
