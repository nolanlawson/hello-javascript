hello-javascript
====

A simple JavaScript module that demonstrates how to write a JavaScript library that can be published in various formats (AMD, UMD, CommonJS, ES6 modules, globals) and to various repositories (npm, Bower, jspm).

All this module does is export a function that prints out `"hello javascript!"`.

Instructions for module authors
----

### Building

`npm run build` or `yarn build` will build the Node-ready and browser-ready versions, which are written to the `dist-node` and `dist` directories.


### Publishing

First, run `npm run build`, then `git commit` the built files. (Yes, we're checking the built files into Git for the benefit of Github and Bower.)

Then do `npm version patch|minor|major` to create the npm version as well as the Git tag. Then `git push origin master --tags`, run `npm publish`, and you're good to go!

For Bower, you will also need to register your module using the [steps described here](http://bower.io/docs/creating-packages/).

Instructions for module users
---

_Module authors: copy-paste these instructions when you publish. This module is not actually published anywhere._

You can install this module in a variety of ways:

### npm

On the command line, run:

```
npm install hello-javascript
```

### yarn

```
  yarn add hello-javascript
  yarn
```
  
Then you can build with Browserify/Webpack using `require('hello-javascript')`, or you can include it directly as a `<script>` tag via the `dist/hello-javascript.js` file. For Rollup users, it uses a `"jsnext:main"` field, so you can directly include the ES6 source.

### Direct download

Download either the unminified `hello-javascript.js` file or the minified `hello-javascript.min.js` file from the [Github releases page](https://github.com/nolanlawson/hello-javascript/releases).

### Bower

```
bower install hello-javascript
```

Then use the `dist/hello-javascript.js` as a `<script>` tag inside your HTML page.

### jspm

```
jspm install hello-javascript
```

Then you can use `dist/hello-javascript.js`.

Why?
---

Writing JavaScript libraries has become complicated. I'm hoping this repository can serve as a [Rosetta Stone](https://en.wikipedia.org/wiki/Rosetta_Stone) so that newbie JavaScript authors have an idea of how to build their code for distribution in various channels.

Missing something?
-----

Open a pull request! I'm sure there is some exotic publishing mechanism that I forgot about. :)
