## Tooling

### Testing

* Unit Testing / Test Runner
  * [Jest](https://facebook.github.io/jest/)
  * [AVA](https://github.com/avajs/ava)
  * [Mocha](https://mochajs.org/) + [Chai](http://chaijs.com/)
  * [Cypress](https://www.cypress.io/)
  * [Karma](https://karma-runner.github.io)
* Web Testing
  * Integration Testing
    * Components - [Enzyme](http://airbnb.io/enzyme/)
    * Reducers
      * [redux-test-utils](https://www.npmjs.com/package/redux-test-utils) + [enzyme-redux](https://www.npmjs.com/package/enzyme-redux)
      * [redux-testkit](https://www.npmjs.com/package/redux-testkit)
  * Functional Testing / E2E Testing
    * Headless Browser Automation
      * DevTools API
        * Headless Chrome - [Puppeteer](https://github.com/GoogleChrome/puppeteer) / [Chromy](https://www.npmjs.com/package/chromy)
          * [End-to-end Tests that Don’t Suck with Puppeteer](https://ropig.com/blog/end-end-tests-dont-suck-puppeteer/)
          * AWS Lambda - [Chromeless](https://www.npmjs.com/package/chromeless)
        * electron-prebuilt - [Nightmare](https://github.com/segmentio/nightmare)
      * WebDriver API - [Selenium WebDriverJS](https://github.com/SeleniumHQ/selenium/wiki/WebDriverJs) / [WebDriverIO](http://webdriver.io/) / [Nightwatch.js](http://nightwatchjs.org/) / [CasperJS](http://casperjs.org/) / [Protractor](http://www.protractortest.org/)
          * AWS Lambda - [Lambdium](https://github.com/smithclay/lambdium)
    * Cloud - [BrowserStack Automate](https://www.browserstack.com/automate) / [Sauce Labs](https://saucelabs.com/open-source#automated-testing-platform)
  * Visual Testing
    * [React Storybook](https://storybooks.js.org/) / [React Cosmos](https://github.com/react-cosmos/react-cosmos)
    * [BrowserStack](https://www.browserstack.com/)
  * Monkey Testing
    * [gremlins.js](https://www.npmjs.com/package/gremlins.js)
  * Headless Browsers
    * Browsers
      * Chromium - [Headless Chrome/Chromium](https://developers.google.com/web/updates/2017/04/headless-chrome)
      * Chromium + Node.js - [electron-prebuilt](https://www.npmjs.com/package/electron)
      * WebKit - [PhantomJS](http://phantomjs.org/)
        * [Why you should stop using PhantomJS](https://blog.phantombuster.com/why-you-should-stop-using-phantomjs-f5c5f2717209)
      * Gecko - [SlimerJS](https://slimerjs.org/)
    * In-memory X11 Display Server
      * [xvfb](https://en.wikipedia.org/wiki/Xvfb) - [xvfb-run](http://manpages.ubuntu.com/manpages/trusty/man1/xvfb-run.1.html) / [headless](https://www.npmjs.com/package/headless)
    * Docker
      * [lighthouse-ci/builder/Dockerfile.headless](https://github.com/ebidel/lighthouse-ci/blob/master/builder/Dockerfile.headless#L16)
      * [electron-headless](https://hub.docker.com/r/dannysu/electron-headless/~/dockerfile/)
* Server-side Testing
  * Functional Testing
    * [supertest](https://www.npmjs.com/package/supertest)
  * Load Testing
    * [k6](https://k6.io/)
    * [loadtest](https://www.npmjs.com/package/loadtest)
* Benchmark Testing
  * JS
    * [Benchmark.js](https://benchmarkjs.com/)
    * [Speedracer](https://github.com/ngryman/speedracer)
    * [stats.js](https://github.com/mrdoob/stats.js)
  * Network
    * [wrk](https://github.com/wg/wrk) / [httpstat](https://github.com/reorx/httpstat)
* [Test Doubles](https://martinfowler.com/bliki/TestDouble.html) ([Fakes, Mocks, Stubs](https://dev.to/milipski/test-doubles---fakes-mocks-and-stubs) and Spies)
  * Fake Data
    * [Faker.js](https://github.com/Marak/Faker.js) / [Chance.js](http://chancejs.com/)
    * [JSON Schema Faker](https://www.npmjs.com/package/json-schema-faker)
    * [placeholder.com](https://placeholder.com/)
  * HTTP Mocking - [Nock](https://www.npmjs.com/package/nock)
  * Monkey Patching - [Mockery](https://www.npmjs.com/package/mockery), [babel-plugin-rewire](https://www.npmjs.com/package/babel-plugin-rewire)
  * [SinonJS](http://sinonjs.org/) / [testdouble.js](https://www.npmjs.com/package/testdouble)
    * [Best Practices for Spies, Stubs and Mocks in Sinon.js](https://semaphoreci.com/community/tutorials/best-practices-for-spies-stubs-and-mocks-in-sinon-js)
    * [testdouble.js vs. sinon.js](http://blog.testdouble.com/posts/2016-03-13-testdouble-vs-sinon.html)
* Analysis
  * Code Coverage
    * [Istanbul](https://istanbul.js.org/)
  * Software Complexity
    * [escomplex](https://www.npmjs.com/package/escomplex) / [complexity-report](https://www.npmjs.com/package/complexity-report)
  * Node.js Security
    * [nsp](https://www.npmjs.com/package/nsp) / [snyk](https://www.npmjs.com/package/snyk)
      * [NSP Advisories](https://nodesecurity.io/advisories/) / [Snyk - Vulnerability DB](https://snyk.io/vuln/)
  * Web Page
    * [Lighthouse](https://developers.google.com/web/tools/lighthouse/) / [pwmetrics](https://github.com/paulirish/pwmetrics)
    * [PageSpeed Insights](https://developers.google.com/speed/pagespeed/)
    * [Varvy SEO tool](https://varvy.com/)

\>\> Return to [Table of Contents](#table-of-contents)

### Documentation

* JS
  * [JSDoc3](http://usejsdoc.org/) + [documentation.js](http://documentation.js.org/) / [jsdox](http://jsdox.org/) / [dox](https://www.npmjs.com/package/dox)
  * [ESDoc](https://esdoc.org/)
  * [React DocGen](https://www.npmjs.com/package/react-docgen)
* API
  * [apiDoc](http://apidocjs.com/)
  * [GraphQL Voyager](https://github.com/APIs-guru/graphql-voyager)
* CLI
  * [Ronn](http://rtomayko.github.io/ronn/)
  * [Docopt](http://docopt.org/)
* Style Guide
  * Markdown + JSX - [docz](https://www.docz.site/)
  * JS - [Storybook](https://storybook.js.org/)
  * JS comments - [React Styleguidist](https://react-styleguidist.js.org/)
  * CSS comments - [KSS (Knyle Style Sheets)](http://warpspire.com/kss/)
    * [kss-node](http://kss-node.github.io/kss-node/)
    * [SC5 Style Guide Generator](http://styleguide.sc5.io/)
* Writing
  * Static Web Generator - [GitBook](https://www.npmjs.com/package/gitbook) / [ReadMe](https://readme.io/)
  * Client-side Rendering - [Docute](https://docute.js.org) / [Docsify](https://docsify.js.org)

\>\> Return to [Table of Contents](#table-of-contents)

### Toolchain

* Compiler / Transpiler / Preprocessor
  * [Babel](https://babeljs.io)
    * [Setting up ES6](https://leanpub.com/setting-up-es6/read)
    * [Babel User Handbook](https://github.com/thejameskyle/babel-handbook/blob/master/translations/en/user-handbook.md), [Babel Plugin Handbook](https://github.com/thejameskyle/babel-handbook/blob/master/translations/en/plugin-handbook.md)
    * Presets
      * [Preset Env](https://babeljs.io/docs/en/next/babel-preset-env.html)
        * [Browserslist](https://github.com/ai/browserslist)
      * [Preset React](http://babeljs.io/docs/plugins/preset-react/)
      * [React Optimize](https://github.com/thejameskyle/babel-react-optimize)
    * Plugins
      * Proposals
        * [Babel progress on ECMAScript proposals](https://github.com/babel/proposals)
        * Shims - [@babel/polyfill](https://github.com/babel/babel/tree/master/packages/babel-polyfill) ([useBuiltIns](https://babeljs.io/docs/en/next/babel-preset-env.html#usebuiltins)) / [core-js](https://github.com/zloirock/core-js)
          * async/await - [fast-async](https://github.com/MatAtBread/fast-async) ([NoDent](https://www.npmjs.com/package/nodent))
        * [Stage 3](http://babeljs.io/docs/plugins/preset-stage-3/), [Stage 2](http://babeljs.io/docs/plugins/preset-stage-2/), [Stage 1](http://babeljs.io/docs/plugins/preset-stage-1/), [Stage 0](http://babeljs.io/docs/plugins/preset-stage-0/)
          * [Class properties](http://babeljs.io/docs/plugins/transform-class-properties/)
          * [Object rest spread](http://babeljs.io/docs/plugins/transform-object-rest-spread/)
          * [Legacy Decorator](https://www.npmjs.com/package/babel-plugin-transform-decorators-legacy) / [Stage 2 Decorators](http://babeljs.io/docs/plugins/transform-decorators/)
          * Dynamic Import- [Syntax](https://www.npmjs.com/package/babel-plugin-syntax-dynamic-import),  [For Node.js](https://www.npmjs.com/package/babel-plugin-dynamic-import-node)
          * [Optional Chaining Operator](https://www.npmjs.com/package/babel-plugin-transform-optional-chaining)
      * Node.js
        * [add-module-exports](https://github.com/59naga/babel-plugin-add-module-exports)
        * [Root Import](https://github.com/entwicklerstube/babel-plugin-root-import) / [Webpack Alias](https://www.npmjs.com/package/babel-plugin-webpack-alias)
      * React
        * [JSX Control Statements](https://www.npmjs.com/package/jsx-control-statements)
        * [React CSS Modules](https://github.com/gajus/babel-plugin-react-css-modules)
      * Libraries
        * [lodash](https://www.npmjs.com/package/babel-plugin-lodash), [ramda](https://www.npmjs.com/package/babel-plugin-ramda)
      * Optimization
        * [transform-remove-console](https://www.npmjs.com/package/babel-plugin-transform-remove-console)
  * [TypeScript](http://www.typescriptlang.org/)
    * [TypeScript: the missing introduction](https://jameshenry.blog/typescript-the-missing-introduction/)
  * [PostCSS](https://github.com/postcss/postcss)
    * Standards
      * [Autoprefixer](https://github.com/postcss/autoprefixer)
      * [CSSNext](http://cssnext.io/) / [postcss-preset-env](https://preset-env.cssdb.org/)
      * [Will Change](https://www.npmjs.com/package/postcss-will-change)
      * [Normalize](https://www.npmjs.com/package/postcss-normalize)
    * Utilities
      * [Utility Library](https://www.npmjs.com/package/postcss-utilities), [Rucksack](http://simplaio.github.io/)
      * [LostGrid](http://lostgrid.org/)
      * [Quantity Queries](https://github.com/pascalduez/postcss-quantity-queries)
      * [Easing Gradients](https://www.npmjs.com/package/postcss-easing-gradients)
      * [Pxtorem](https://www.npmjs.com/package/postcss-pxtorem)
      * [Brand Colors](https://www.npmjs.com/package/postcss-brand-colors) / [Nippon Color](https://www.npmjs.com/package/postcss-nippon-color) / [Google Color](https://www.npmjs.com/package/postcss-google-color)
      * [Contrast](https://www.npmjs.com/package/postcss-contrast) / [Get Color](https://www.npmjs.com/package/postcss-get-color)
    * Assets
      * [Assets](https://www.npmjs.com/package/postcss-assets)
      * [Inline SVG](https://www.npmjs.com/package/postcss-inline-svg), [SVGO](https://www.npmjs.com/package/postcss-svgo)
      * [Font Magician](https://www.npmjs.com/package/postcss-font-magician)
    * Syntax
      * [PreCSS](https://www.npmjs.com/package/precss)
      * [SCSS Parser](https://www.npmjs.com/package/postcss-scss)
      * [JS](https://www.npmjs.com/package/postcss-js)
  * [node-sass](https://www.npmjs.com/package/node-sass)
  * [PostHTML](https://www.npmjs.com/package/posthtml)
* Loader / Builder / Bundler
  * [Webpack](https://webpack.js.org/concepts/)
    * [webpack-howto](https://github.com/petehunt/webpack-howto)
      * [SurviveJS Webpack](https://survivejs.com/webpack/what-is-webpack/)
      * [webpack-blocks](https://github.com/andywer/webpack-blocks)
    * Loaders
      * [babel-loader](https://www.npmjs.com/package/babel-loader), [ts-loader](https://www.npmjs.com/package/ts-loader) / [awesome-typescript-loader](https://www.npmjs.com/package/awesome-typescript-loader), [vue-loader](https://www.npmjs.com/package/vue-loader)
        * [imports-loader](https://www.npmjs.com/package/imports-loader)
          * [Granular Shimming](https://webpack.js.org/guides/shimming/#granular-shimming)
        * [exports-loader](https://webpack.js.org/loaders/exports-loader/)
          * [Global Exports](https://webpack.js.org/guides/shimming/#global-exports)
      * [css-loader](https://www.npmjs.com/package/css-loader), [style-loader](https://www.npmjs.com/package/style-loader) / [isomorphic-style-loader](https://www.npmjs.com/package/isomorphic-style-loader)
        * [postcss-loader](https://www.npmjs.com/package/postcss-loader), [scss-loader](https://www.npmjs.com/package/sass-loader), [less-loader](https://www.npmjs.com/package/less-loader)
        * [resolve-url-loader](https://www.npmjs.com/package/resolve-url-loader)
      * [workerize-loader](https://www.npmjs.com/package/workerize-loader) / [worker-loader](https://www.npmjs.com/package/worker-loader)
      * [raw-loader](https://www.npmjs.com/package/raw-loader)
        * [html-loader](https://www.npmjs.com/package/html-loader)
          * [markdown-loader](https://www.npmjs.com/package/markdown-loader) / [handlebars-loader](https://www.npmjs.com/package/handlebars-loader)
        * [shader-loader](https://www.npmjs.com/package/shader-loader) / [glslify-loader](https://www.npmjs.com/package/glslify-loader)
      * [image-webpack-loader](https://www.npmjs.com/package/image-webpack-loader) / [img-loader](https://www.npmjs.com/package/img-loader)
      * [svg-react-loader](https://www.npmjs.com/package/svg-react-loader), [react-markdown-loader](https://www.npmjs.com/package/react-markdown-loader)
      * [url-loader](https://www.npmjs.com/package/url-loader), [svg-url-loader](https://www.npmjs.com/package/svg-url-loader)
      * [file-loader](https://www.npmjs.com/package/file-loader)
      * [thread-loader](https://www.npmjs.com/package/thread-loader), [cache-loader](https://www.npmjs.com/package/cache-loader), [val-loader](https://www.npmjs.com/package/val-loader)
    * Plugins
      * [Extract Text Plugin](https://www.npmjs.com/package/extract-text-webpack-plugin), [Webpack Manifest Plugin](https://www.npmjs.com/package/webpack-manifest-plugin)
      * [Copy Webpack Plugin](https://github.com/kevlened/copy-webpack-plugin), [Clean Webpack Plugin](https://www.npmjs.com/package/clean-webpack-plugin)
      * [HTML Webpack Plugin](https://www.npmjs.com/package/html-webpack-plugin)
        * [HTML Webpack Template](https://github.com/jaketrent/html-webpack-template)
        * Plugins
          * [Favicons](https://www.npmjs.com/package/favicons-webpack-plugin)
          * [Harddisk](https://www.npmjs.com/package/html-webpack-harddisk-plugin)
          * [Inline Source](https://www.npmjs.com/package/html-webpack-inline-source-plugin), [Preload](https://www.npmjs.com/package/preload-webpack-plugin)
          * [Include Assets](https://www.npmjs.com/package/html-webpack-include-assets-plugin) + [Exclude Assets](https://www.npmjs.com/package/html-webpack-exclude-assets-plugin)
          * [Inline Chunk Manifest](https://www.npmjs.com/package/inline-chunk-manifest-html-webpack-plugin)
      * [Define Plugin](https://webpack.js.org/plugins/define-plugin/) / [Environment Plugin](https://webpack.js.org/plugins/environment-plugin/)
      * [Provide Plugin](https://webpack.js.org/plugins/provide-plugin/)
        * [Shimming Global](https://webpack.js.org/guides/shimming/)
      * [Ignore Plugin](https://webpack.js.org/plugins/ignore-plugin/), [Watch Ignore Plugin](https://webpack.js.org/plugins/watch-ignore-plugin/)
      * [Module Concatenation Plugin](https://webpack.js.org/plugins/module-concatenation-plugin/), [Lodash Plugin](https://www.npmjs.com/package/lodash-webpack-plugin)
      * [UglifyJS Webpack Plugin](https://www.npmjs.com/package/uglifyjs-webpack-plugin) / [Babel Minify Webpack Plugin](https://www.npmjs.com/package/babel-minify-webpack-plugin)
      * [Workbox Webpack Plugins](https://developers.google.com/web/tools/workbox/modules/workbox-webpack-plugin), [Offline Plugin](https://www.npmjs.com/package/offline-plugin)
      * [Bundle Analyzer](https://www.npmjs.com/package/webpack-bundle-analyzer)
      * [Fork TS Checker Webpack Plugin](https://www.npmjs.com/package/fork-ts-checker-webpack-plugin), [HappyPack](https://www.npmjs.com/package/happypack)
  * [Rollup](https://rollupjs.org/)
    * [Webpack and Rollup: the same but different](https://medium.com/webpack/webpack-and-rollup-the-same-but-different-a41ad427058c)
* Formatter
  * ESLint with autofix feature - see Static Analysis
  * [Prettier](https://www.npmjs.com/package/prettier)
    * [prettier-eslint](https://www.npmjs.com/package/prettier-eslint)
  * Codemod - [Effective JavaScript Codemods](https://medium.com/@cpojer/effective-javascript-codemods-5a6686bb46fb)
    * [jscodeshift](https://www.npmjs.com/package/jscodeshift)
    * [react-codemod](https://www.npmjs.com/package/react-codemod)
    * [Recast](https://www.npmjs.com/package/recast)
  * [stylefmt](https://www.npmjs.com/package/stylefmt)
* Static Analysis
  * [ESLint](http://eslint.org/)
    * [ESLint Rules](http://eslint.org/docs/rules/)
      * [eslint-index](https://www.npmjs.com/package/eslint-index), [eslint-find-rules](https://www.npmjs.com/package/eslint-find-rules)
    * Plugins
      * [prettier](https://www.npmjs.com/package/eslint-plugin-prettier)
      * [babel](https://www.npmjs.com/package/babel-eslint), [import](https://www.npmjs.com/package/eslint-plugin-import), [eslint-comments](https://www.npmjs.com/package/eslint-plugin-eslint-comments), [unicorn](https://www.npmjs.com/package/eslint-plugin-unicorn), [no-use-extend-native](https://www.npmjs.com/package/eslint-plugin-no-use-extend-native)
      * [filenames](https://www.npmjs.com/package/eslint-plugin-filenames)
        * [eslint-import-resolver-webpack](https://www.npmjs.com/package/eslint-import-resolver-webpack)
      * [compat](https://www.npmjs.com/package/eslint-plugin-compat)
      * [node](https://www.npmjs.com/package/eslint-plugin-node), [security](https://www.npmjs.com/package/eslint-plugin-security)
      * [react](https://www.npmjs.com/package/eslint-plugin-react), [jsx-a11y](https://www.npmjs.com/package/eslint-plugin-jsx-a11y), [graphql](https://www.npmjs.com/package/eslint-plugin-graphql), [mongodb](https://www.npmjs.com/package/eslint-plugin-mongodb)
      * [jsdoc](https://www.npmjs.com/package/eslint-plugin-jsdoc), [flowtype](https://github.com/gajus/eslint-plugin-flowtype)
      * [jest](https://www.npmjs.com/package/eslint-plugin-jest), [ava](https://www.npmjs.com/package/eslint-plugin-ava), [mocha](https://www.npmjs.com/package/eslint-plugin-mocha), [chai-expect](https://www.npmjs.com/package/eslint-plugin-chai-expect)
      * [fp](https://www.npmjs.com/package/eslint-plugin-fp), [lodash](https://www.npmjs.com/package/eslint-plugin-lodash), [lodash-fp](https://www.npmjs.com/package/eslint-plugin-lodash-fp), [immutable](https://www.npmjs.com/package/eslint-plugin-immutable)
      * [promise](https://www.npmjs.com/package/eslint-plugin-promise), [optimize-regex](https://www.npmjs.com/package/eslint-plugin-optimize-regex)
    * Presets
      * [eslint-config-webcube](./packages/eslint-config-webcube/) (Author's own project)
      * [eslint-config-airbnb](https://www.npmjs.com/package/eslint-config-airbnb)
      * [eslint-config-react-app](https://github.com/facebookincubator/create-react-app/tree/master/packages/eslint-config-react-app)
  * [Flow](https://flow.org)
    * [flow-typed](https://github.com/flowtype/flow-typed)
    * [Flow Runtime](https://www.npmjs.com/package/babel-plugin-flow-runtime)
  * [StyleLint](http://stylelint.io/)
    * [doiuse](https://www.npmjs.com/package/doiuse)
    * [Colorguard](https://www.npmjs.com/package/colorguard)
    * [postcss-bem-linter](https://www.npmjs.com/package/postcss-bem-linter)
  * [HTMLHint](https://github.com/yaniswang/HTMLHint)
* Minifier / Compressor / Optimizer
  * [Prepack](https://prepack.io/)
  * [babel-minify](https://github.com/babel/minify) / [uglify-es](https://github.com/mishoo/UglifyJS2/tree/harmony) / [UglifyJS 3](https://github.com/mishoo/UglifyJS2) / [UglifyJS 2](https://github.com/mishoo/UglifyJS2/tree/v2.x)
  * [cssnano](http://cssnano.co/) / [clean-css](https://www.npmjs.com/package/clean-css) / [CSSO](https://www.npmjs.com/package/csso)
  * [HTMLMinifier](https://github.com/kangax/html-minifier)
  * [Critical](https://www.npmjs.com/package/critical) / [Penthouse](https://www.npmjs.com/package/penthouse)
  * [imagemin](https://www.npmjs.com/package/imagemin)
    * [gifsicle](https://github.com/kevva/imagemin-gifsicle)
    * [jpegtran](https://www.npmjs.com/package/imagemin-jpegtran) / [mozjpeg](https://github.com/imagemin/imagemin-mozjpeg)
    * [optipng](https://github.com/kevva/imagemin-optipng) / [pngquant](https://www.npmjs.com/package/imagemin-pngquant)
    * [svgo](https://github.com/kevva/imagemin-svgo)
    * [webp](https://www.npmjs.com/package/imagemin-webp)
  * [fontmin](https://www.npmjs.com/package/fontmin), [font-spider](https://www.npmjs.com/package/font-spider)
* Task Automation
  * [npm-run-script](https://docs.npmjs.com/cli/run-script), [npm-scripts](https://docs.npmjs.com/misc/scripts)
    * [task automation with npm run](http://substack.net/task_automation_with_npm_run), \
      [How to Use npm as a Build Tool](https://www.keithcirkel.co.uk/how-to-use-npm-as-a-build-tool/)
      * [Why I Left Gulp and Grunt for npm Scripts](https://medium.freecodecamp.com/why-i-left-gulp-and-grunt-for-npm-scripts-3d6853dd22b8)
    * Git Hooks
      * [Husky](https://github.com/typicode/husky)
      * [lint-staged](https://www.npmjs.com/package/lint-staged)
        * [Make linting great again!](https://medium.com/@okonetchnikov/make-linting-great-again-f3890e1ad6b8)
    * Environment Variables - [env-cmd](https://www.npmjs.com/package/env-cmd), [cross-env](https://www.npmjs.com/package/cross-env)
    * [get-port](https://www.npmjs.com/package/get-port), [public-ip](https://www.npmjs.com/package/public-ip)
  * [Gulp](http://gulpjs.com/)
    * [gulp - The vision, history, and future of the project](https://medium.com/@contrahacks/gulp-3828e8126466)
    * [Why you shouldn’t create a gulp plugin](http://blog.overzealous.com/post/74121048393/why-you-shouldnt-create-a-gulp-plugin-or-how-to)
    * [Gulpfile API](https://github.com/gulpjs/gulp/blob/master/docs/API.md)
    * Utilities
      * [The Problem with gulp-util](https://medium.com/gulpjs/gulp-util-ca3b1f9f9ac5)
      * [through2](https://www.npmjs.com/package/through2), [gulp-load-plugins](https://www.npmjs.com/package/gulp-load-plugins)
      * [gulp-size](https://www.npmjs.com/package/gulp-size), [gulp-count](https://www.npmjs.com/package/gulp-count), [gulp-notify](https://www.npmjs.com/package/gulp-notify)
      * [gulp-debug](https://www.npmjs.com/package/gulp-debug)
      * [gulp-if](https://www.npmjs.com/package/gulp-if), [gulp-filter](https://www.npmjs.com/package/gulp-filter), [merge-stream](https://www.npmjs.com/package/merge-stream)
      * [gulp-changed](https://www.npmjs.com/package/gulp-changed) / [gulp-cached](https://www.npmjs.com/package/gulp-cached)
      * [gulp-exec](https://www.npmjs.com/package/gulp-exec), [gulp-git](https://www.npmjs.com/package/gulp-git)
      * [gulp-rename](https://www.npmjs.com/package/gulp-rename)
      * [gulp-replace](https://www.npmjs.com/package/gulp-replace/) / [gulp-inject](https://www.npmjs.com/package/gulp-inject) / [gulp-useref](https://www.npmjs.com/package/gulp-useref), [gulp-inline-source](https://www.npmjs.com/package/gulp-inline-source/)
      * [gulp-sourcemaps](https://www.npmjs.com/package/gulp-sourcemaps)

\>\> Return to [Table of Contents](#table-of-contents)

### Workflow

* Development
  * Micro Generator
    * [Plop](https://plopjs.com)
  * Live Reload / Watch / Preview
    * [webpack-serve](https://github.com/webpack-contrib/webpack-serve)
    * [webpack-dev-server](https://www.npmjs.com/package/webpack-dev-server)
      * [webpack-dashboard](https://www.npmjs.com/package/webpack-dashboard)
      * [webpack-dev-middleware](https://www.npmjs.com/package/webpack-dev-middleware)
    * [Hot Module Replacement](https://webpack.js.org/guides/hot-module-replacement/) / [React Hot Loader](http://gaearon.github.io/react-hot-loader/)
    * [Browsersync](https://www.npmjs.com/package/browser-sync)
    * Electron - [Electron Connect](https://www.npmjs.com/package/electron-connect)
    * React Native - [Expo](https://expo.io/)
    * Node.js - [nodemon](https://www.npmjs.com/package/nodemon)
  * Dev Tools
    * [Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/) / [Firefox Developer Tools](https://developer.mozilla.org/en-US/docs/Tools) / [Safari Web Inspector](https://developer.apple.com/library/content/documentation/AppleApplications/Conceptual/Safari_Developer_Guide/) / [Microsoft Edge F12 Dev Tools](https://docs.microsoft.com/en-us/microsoft-edge/f12-devtools-guide)
      * Console - [Console API](https://developers.google.com/web/tools/chrome-devtools/console/console-reference), [Command Line API](https://developers.google.com/web/tools/chrome-devtools/console/command-line-reference)
    * Third-party Panels
      * [React DevTools](https://github.com/facebook/react-devtools) / [AngularJS Batarang](https://chrome.google.com/webstore/detail/angularjs-batarang/ighdmehidhipcmcojjgiloacoafjmpfk) / [Augury](https://chrome.google.com/webstore/detail/augury/elgalmkoelokbchhkhacckoklkejnhcd) / [Vue.js DevTools](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd)
      * [React Perf](https://chrome.google.com/webstore/detail/react-perf/hacmcodfllhbnekmghgdlplbdnahmhmm)
      * [Redux DevTools](https://github.com/gaearon/redux-devtools)
      * [Immutable DevTools](https://github.com/andrewdavey/immutable-devtools), [Immutable.js Object Formatter](https://chrome.google.com/webstore/detail/immutablejs-object-format/hgldghadipiblonfkkicmgcbbijnpeog)
      * [Apollo Client Devtools](https://github.com/apollographql/apollo-client-devtools), [GraphQL Network](https://github.com/Ghirro/graphql-network)
      * [JWT Inspector](https://jwtinspector.io/)
      * [WebGL Insight](https://github.com/3Dparallax/insight/), [Three.js Editor Extension](https://chrome.google.com/webstore/detail/threejs-editor-extension/fbgbekpggeldiacgjkacbkkcbjhmakea)
    * [Reactotron](https://github.com/infinitered/reactotron)
    * Electron - [Devtron](https://github.com/electron/devtron)
    * [React Native Debugger](https://github.com/jhen0409/react-native-debugger)
  * HTTP Inspector
    * [Paw](https://paw.cloud/) / [Postman](https://www.getpostman.com/) / [HTTPie](https://github.com/jakubroztocil/httpie)
  * Debugging Proxy
    * [AnyProxy](http://anyproxy.io/en.html) / [Fiddler](http://www.telerik.com/fiddler)
    * [Tamper Chrome](https://github.com/google/tamperchrome)
* Deployment
  * Publishing App
    * Server-side Rendering
      * [Hypernova](https://github.com/airbnb/hypernova)
      * [React Isomorphic Render](https://www.npmjs.com/package/react-isomorphic-render)
      * [React Engine](https://www.npmjs.com/package/react-engine)
      * [Express React Views](https://www.npmjs.com/package/express-react-views)
    * Static Web
      * Dynamic Routing + CDN
        * [Superstatic](https://www.npmjs.com/package/superstatic)
      * Object Storage + CDN
        * Global
          * [Amazon S3 + CloudFront](http://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html) - [aws-sdk](https://www.npmjs.com/package/aws-sdk) / [awscli](https://github.com/aws/aws-cli)
          * [Google Cloud Storage + Cloud CDN](https://cloud.google.com/storage/docs/hosting-static-website) - [google-cloud](https://www.npmjs.com/package/google-cloud) / [gcloud](https://cloud.google.com/sdk/gcloud/)
          * [Firebase Hosting](https://firebase.google.com/products/hosting/) - [firebase-tools](https://www.npmjs.com/package/firebase-tools)
          * [Netlify](https://www.netlify.com/) - [netlify-cli](https://www.npmjs.com/package/netlify-cli)
          * [Surge](https://surge.sh/) - [surge cli client](https://www.npmjs.com/package/surge)
        * China
          * [阿里云 OSS + CDN](https://help.aliyun.com/document_detail/31872.html) - [aliyun-sdk](https://www.npmjs.com/package/aliyun-sdk) / [oss-nodejs-sdk](https://www.npmjs.com/package/ali-oss)
          * [腾讯云 COS + CDN](https://www.qcloud.com/document/product/436/9512) - [cos-nodejs-sdk-v5](https://www.npmjs.com/package/cos-nodejs-sdk-v5)
    * Packaged App
      * [Electron Builder](https://www.npmjs.com/package/electron-builder)
        * [Auto Update](https://github.com/electron-userland/electron-builder/wiki/Auto-Update)
      * [CodePush](https://www.npmjs.com/package/react-native-code-push)
  * DevOps
    * Process Supervisor
      * [pm2](http://pm2.keymetrics.io/)
        * [pm2-docker](http://pm2.keymetrics.io/docs/usage/docker-pm2-nodejs/)
        * [Process File](http://pm2.keymetrics.io/docs/usage/application-declaration/)
    * Containers
      * [Docker](https://docs.docker.com/engine/reference/builder/)
        * Learning
          * [Play with docker classroom](http://training.play-with-docker.com/)
          * [Docker Curriculum](https://github.com/prakhar1989/docker-curriculum)
          * [Docker Cheat Sheet](https://github.com/wsargent/docker-cheat-sheet) / [Docker Cheat Sheet](http://docker.jens-piegsa.com/)
        * [Dockerfile reference](https://docs.docker.com/engine/reference/builder/)
        * [Docker run reference](https://docs.docker.com/engine/reference/run/)
        * [Docker Compose](https://docs.docker.com/compose/overview/)
      * Docker Images
        * [node](https://github.com/nodejs/docker-node) / [risingstack/alpine](https://hub.docker.com/r/risingstack/alpine/) / [keymetrics/pm2-docker-alpine](https://hub.docker.com/r/keymetrics/pm2-docker-alpine/)
        * [docker-lambda](https://github.com/lambci/docker-lambda)
    * Container Clusters
      * [Docker Engine in Swarm Mode](https://docs.docker.com/engine/swarm/)
        * [Compose file reference](https://docs.docker.com/compose/compose-file/)
        * [wait-for-it.sh](https://github.com/vishnubob/wait-for-it) / [dockerize](https://github.com/jwilder/dockerize)
      * [Kubernetes](https://kubernetes.io/)
        * [Kubernetes Cheat Sheet](http://k8s.info/cs.html)
    * PaaS
      * Global
        * [now](https://zeit.co/now)
        * [heroku](heroku.com) - [heroku-cli](https://devcenter.heroku.com/articles/heroku-cli#getting-started)
      * China
        * [LeanCloud-云引擎](https://leancloud.cn/docs/leanengine_overview.html) ([云函数](https://leancloud.cn/docs/leanengine_cloudfunction_guide-node.html), [网站托管](https://leancloud.cn/docs/leanengine_webhosting_guide-node.html)) - [lean-cli](https://leancloud.cn/docs/leanengine_cli.html)
* Monitoring
  * Error Tracking
    * [Capturing client-side JavaScript errors](https://www.thoughtworks.com/radar/techniques/capturing-client-side-javascript-errors), [Front-End Error Handling](https://staticapps.org/articles/front-end-error-handling/)
      * [A Guide to Proper Error Handling in JavaScript](https://www.sitepoint.com/proper-error-handling-javascript/)
    * Services
      * [TrackJS](https://trackjs.com/) / [Errorception](https://errorception.com/)
      * [Sentry](https://sentry.io/for/javascript/) / [Rollbar](https://rollbar.com/docs/notifier/rollbar.js/) / [Bugsnag](https://docs.bugsnag.com/platforms/browsers/) / [Airbrake](https://airbrake.io/languages/javascript_exception_handler) / [Raygun](https://raygun.com/)
  * Logging
    * Global
      * [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/) / [Google Stackdriver](https://cloud.google.com/stackdriver/)
      * [PM2 Plus](https://pm2.io/plus/)
    * China
      * [阿里云-云监控](https://www.aliyun.com/product/jiankong) / [腾讯云-基础监控 BCM](https://www.qcloud.com/product/bcm)
  * APM (Application Performance Management)
    * Global
      * [New Relic](https://newrelic.com/) / [AppDynamics](https://www.appdynamics.com/) / [Datadog APM](https://www.datadoghq.com/apm/)
      * [Pingdom](https://www.pingdom.com/) / [SpeedCurve](https://speedcurve.com/) / [AppNeta](https://www.appneta.com/)
      * [Trace](https://trace.risingstack.com)
    * China
      * [OneAPM](https://www.oneapm.com/) / [听云](http://www.tingyun.com/)
      * [监控宝](https://www.jiankongbao.com/) / [百度云观测](http://ce.baidu.com/) / [360网站服务监控](http://jk.cloud.360.cn/) / [腾讯云-云拨测 CAT](https://www.qcloud.com/product/cat)
      * [阿里云 Node.js 性能平台](https://www.aliyun.com/product/nodejs)

\>\> Return to [Table of Contents](#table-of-contents)

### Command-line Environment (Mac)

* Intro
  * [The Art of Command Line](https://github.com/jlevy/the-art-of-command-line)
  * [The Bash Guide](http://guide.bash.academy/)
  * [Linux Shell Scripting Tutorial (LSST)](https://bash.cyberciti.biz/guide/Main_Page)
* Terminal
  * [iTerm2](https://www.iterm2.com/)
    * [iTerm Color Schemes](https://github.com/mbadolato/iTerm2-Color-Schemes)
  * [Hyper](https://hyper.is/)
    * [Awesome Hyper](https://github.com/bnb/awesome-hyper)
* Package Manager
  * [Homebrew](https://brew.sh/)
* Shell
  * [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh)
  * [Spaceship ZSH Theme](https://github.com/denysdovhan/spaceship-zsh-theme)
  * Zsh Plugins
    * [zsh-better-npm-completion](https://github.com/lukechilds/zsh-better-npm-completion)
    * [Awesome Zsh Plugins](https://github.com/unixorn/awesome-zsh-plugins)
* Vim
  * [Vimtutor](http://linuxcommand.org/man_pages/vimtutor1.html)
  * [spf13-vim](https://github.com/spf13/spf13-vim) / [YVim](https://github.com/dexteryy/YVim)
* Git
  * [Git-it](https://github.com/jlord/git-it-electron), [TryGit Simulator](https://try.github.io/)
  * [Become a git guru](https://www.atlassian.com/git/tutorials), [Git Glossary](https://www.atlassian.com/git/glossary)
  * [Pro Git - Index of Commands](https://git-scm.com/book/commands)
  * [commitizen](https://github.com/commitizen/cz-cli)
* [Docker for Mac](https://docs.docker.com/docker-for-mac/)
* [dotfiles](https://dotfiles.github.io/)
* Utilities
  * Analysis - [cloc](https://github.com/AlDanial/cloc/)
  * Finding - [rg (ripgrep)](https://github.com/BurntSushi/ripgrep) / [ag (The Silver Searcher)](https://github.com/ggreer/the_silver_searcher), [peco](https://github.com/peco/peco), [jq](https://stedolan.github.io/jq), [fzf](https://github.com/junegunn/fzf)
  * Processes - [glances](https://github.com/nicolargo/glances) / [vtop](https://www.npmjs.com/package/vtop), [fkill](https://www.npmjs.com/package/fkill-cli)
  * Help - [tldr](https://github.com/tldr-pages/tldr) / [howdoi](https://github.com/gleitz/howdoi)

\>\> Return to [Table of Contents](#table-of-contents)

### Command-line Libraries (Node.js)

* Input
  * Options/Arguments Parser - [minimist](https://www.npmjs.com/package/minimist) / [commander](https://www.npmjs.com/package/commander) / [yargs](https://www.npmjs.com/package/yargs)
  * Interactive - [inquirer](https://www.npmjs.com/package/inquirer)
  * Rapidly Building - [vorpal](https://www.npmjs.com/package/vorpal) / [cli](https://www.npmjs.com/package/cli)
  * Configuration - [Liftoff](https://www.npmjs.com/package/liftoff)
* Output
  * Color / Style - [Chalk](https://www.npmjs.com/package/chalk)
  * Icon - [log-symbols](https://www.npmjs.com/package/log-symbols) / [figures](https://www.npmjs.com/package/figures)
  * Updating Log
    * Low-level - [log-update](https://www.npmjs.com/package/log-update)
    * Indicator - [ora](https://www.npmjs.com/package/ora) / [progress](https://www.npmjs.com/package/progress) / [pace](https://www.npmjs.com/package/pace)
    * Pretty Log - [DraftLogs](https://www.npmjs.com/package/draftlog) / [listr](https://www.npmjs.com/package/listr)
  * Notice - [boxen](https://www.npmjs.com/package/boxen), [cfonts](https://www.npmjs.com/package/cfonts)
  * Columns - [cli-table](https://www.npmjs.com/package/cli-table) / [columnify](https://www.npmjs.com/package/columnify)
  * Curses-like - [blessed](https://www.npmjs.com/package/blessed)
  * Drawing - [drawille-canvas](https://www.npmjs.com/package/drawille-canvas)
  * Image - [term-img](https://www.npmjs.com/package/term-img)
* Delivery
  * [update-notifier](https://www.npmjs.com/package/update-notifier)
  * Reporting Usage - [insight](https://www.npmjs.com/package/insight)
  * Self-contained Executable - [pkg](https://www.npmjs.com/package/pkg)
* Framework
  * Generator - [Yeoman](http://yeoman.io/authoring/)
* OS
  * Shell Commands - [ShellJS](https://www.npmjs.com/package/shelljs)
  * Filesystem
    * Filesystem API - [fs-extra](https://www.npmjs.com/package/fs-extra) / [fs-jetpack](https://www.npmjs.com/package/fs-jetpack)
    * Wildcard Matching - [glob](https://www.npmjs.com/package/glob) / [globby](https://www.npmjs.com/package/globby), [matcher](https://www.npmjs.com/package/matcher)
    * Virtual Filesystem - [vinyl](https://www.npmjs.com/package/vinyl-fs)
    * Temporary File - [tmp](https://www.npmjs.com/package/tmp)
    * File Locking - [proper-lockfile](https://www.npmjs.com/package/proper-lockfile)
    * Finding - [find-up](https://www.npmjs.com/package/find-up), [readdirp](https://www.npmjs.com/package/readdirp)
    * Watch - [chokidar](https://www.npmjs.com/package/chokidar) / [gaze](https://www.npmjs.com/package/gaze)
  * Local
    * [network-address](https://www.npmjs.com/package/network-address)
    * [clipboardy](https://www.npmjs.com/package/clipboardy)
* API
  * Git - [simple-git](https://www.npmjs.com/package/simple-git) / [nodegit](https://www.npmjs.com/package/nodegit)
  * Docker - [dockerode](https://www.npmjs.com/package/dockerode)
  * SSH - [ssh2](https://www.npmjs.com/package/ssh2)
* Parser
  * JS - [Acorn](https://www.npmjs.com/package/acorn) / [Babylon](https://www.npmjs.com/package/babylon) / [Espree](https://www.npmjs.com/package/espree) / [Esprima](https://www.npmjs.com/package/esprima)

\>\> Return to [Table of Contents](#table-of-contents)

### IDE / Editors

* [VS Code](https://code.visualstudio.com/) Plugins
  * UI
    * [vscode-icons](https://marketplace.visualstudio.com/items?itemName=robertohuertasm.vscode-icons)
    * [Indenticator](https://marketplace.visualstudio.com/items?itemName=SirTori.indenticator)
  * Operating
    * [VSCodeVim](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim)
    * [Search node_modules](https://marketplace.visualstudio.com/items?itemName=jasonnutter.search-node-modules)
    * [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)
    * [npm Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense)
    * [Lorem ipsum](https://marketplace.visualstudio.com/items?itemName=Tyriar.lorem-ipsum) / [Chinese Lorem Ipsum](https://marketplace.visualstudio.com/items?itemName=galend.vsc-lorem-cn)
    * Snippets
      * [JavaScript (ES6) code snippets](https://marketplace.visualstudio.com/items?itemName=xabikos.JavaScriptSnippets)
      * [JavaScript Snippet Pack](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-javascript-snippet-pack)
      * [Reactjs code snippets](https://marketplace.visualstudio.com/items?itemName=xabikos.ReactSnippets)
      * [React Redux ES6 Snippets](https://marketplace.visualstudio.com/items?itemName=timothymclane.react-redux-es6-snippets)
      * [eslint-disable-snippets](https://marketplace.visualstudio.com/items?itemName=drKnoxy.eslint-disable-snippets)
      * [HTML Snippets](https://marketplace.visualstudio.com/items?itemName=abusaidm.html-snippets)
      * [SVG Icons](https://marketplace.visualstudio.com/items?itemName=idleberg.svg-icons)
      * [Icon Fonts](https://marketplace.visualstudio.com/items?itemName=idleberg.icon-fonts)
  * Formatting
    * [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
    * [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) / [stylefmt](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-stylefmt)
    * [EditorConfig](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)
    * [change-case](https://marketplace.visualstudio.com/items?itemName=wmaurer.change-case)
    * [Align](https://marketplace.visualstudio.com/items?itemName=steve8708.Align)
  * Static Analysis
    * [Flow Language Support](https://marketplace.visualstudio.com/items?itemName=flowtype.flow-for-vscode)
    * [Stylelint](https://marketplace.visualstudio.com/items?itemName=shinnn.stylelint)
    * [HTMLHint](https://marketplace.visualstudio.com/items?itemName=mkaufman.HTMLHint)
    * Syntax
      * [CSS Modules](https://marketplace.visualstudio.com/items?itemName=clinyong.vscode-css-modules)
      * [vscode-styled-components](https://marketplace.visualstudio.com/items?itemName=jpoissonnier.vscode-styled-components)
      * [GraphQL for VSCode](https://marketplace.visualstudio.com/items?itemName=kumar-harsh.graphql-for-vscode)
      * [Docker](https://marketplace.visualstudio.com/items?itemName=PeterJausovec.vscode-docker)
  * Docs
    * [Dash](https://marketplace.visualstudio.com/items?itemName=deerawan.vscode-dash)
    * [Regex Previewer](https://marketplace.visualstudio.com/items?itemName=chrmarti.regex)
    * [Color Picker](https://marketplace.visualstudio.com/items?itemName=anseki.vscode-color)
    * [Swagger Viewer](https://marketplace.visualstudio.com/items?itemName=Arjun.swagger-viewer)
    * [API Elements extension](https://marketplace.visualstudio.com/items?itemName=vncz.vscode-apielements)
  * Assistant
    * [Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)
    * [Project Manager](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager)
[Bookmarks](Bookmarks.md)
    * [TODO Highlight](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight)
    * [Quokka.js - Live Scratchpad for JavaScript](https://marketplace.visualstudio.com/items?itemName=WallabyJs.quokka-vscode)
  * Integration
    * VCS
      * [Git Lens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
      * [Git History](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory)
      * [Open in GitHub](https://marketplace.visualstudio.com/items?itemName=ziyasal.vscode-open-in-github)
    * [Share Code](https://marketplace.visualstudio.com/items?itemName=RolandGreim.sharecode)
    * Debug
      * [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)
      * [Node Debug 2](https://marketplace.visualstudio.com/items?itemName=ms-vscode.node-debug2)
      * [Jest](https://marketplace.visualstudio.com/items?itemName=Orta.vscode-jest)
    * [React Native Tools](https://marketplace.visualstudio.com/items?itemName=vsmobile.vscode-react-native)
    * [Cordova Tools](https://marketplace.visualstudio.com/items?itemName=vsmobile.cordova-tools)
    * Write
      * [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)
      * [Mermaid Preview](https://marketplace.visualstudio.com/items?itemName=vstirbu.vscode-mermaid-preview)
* [Atom](https://atom.io/) Plugins
  * UI
    * [fonts](https://atom.io/packages/fonts)
    * [file-icons](https://atom.io/packages/file-icons)
    * [highlight-line](https://atom.io/packages/highlight-line), [highlight-selected](https://atom.io/packages/highlight-selected)
    * [indent-guide-improved](https://atom.io/packages/indent-guide-improved), [trailing-spaces](https://atom.io/packages/trailing-spaces)
  * Operating
    * [vim-mode-plus](https://atom.io/packages/vim-mode-plus), [jumpy](https://atom.io/packages/jumpy)
    * [Sublime-Style-Column-Selection](https://atom.io/packages/Sublime-Style-Column-Selection)
    * [Emmet](https://atom.io/packages/emmet)
    * Snippets
      * [turbo-javascript](https://atom.io/packages/turbo-javascript)
  * Formatting
    * [auto-detect-indentation](https://atom.io/packages/auto-detect-indentation), [editorconfig](https://atom.io/packages/editorconfig)
    * [prettier-atom](https://atom.io/packages/prettier-atom)
    * [atom-stylefmt](https://atom.io/packages/stylefmt) / [postcss-sorting](https://atom.io/packages/postcss-sorting) / [atom-beautify](https://atom.io/packages/atom-beautify)
    * [aligner](https://atom.io/packages/aligner) / [atom-alignment](https://atom.io/packages/atom-alignment)
    * [toggle-quotes](https://atom.io/packages/toggle-quotes)
  * Static Analysis
    * [file-types](https://atom.io/packages/file-types)
    * [language-babel](https://atom.io/packages/language-babel), [atom-ternjs](https://atom.io/packages/atom-ternjs)
    * [language-postcss](https://atom.io/packages/language-postcss)
    * [language-mjml](https://atom.io/packages/language-mjml)
    * [linter-eslint](https://atom.io/packages/linter-eslint), [linter-flow](https://atom.io/packages/linter-flow), [linter-stylelint](https://atom.io/packages/linter-stylelint), [linter-htmlhint](https://atom.io/packages/linter-htmlhint), [linter-mjml](https://atom.io/packages/linter-mjml), [linter-jsonlint](https://atom.io/packages/linter-jsonlint), [linter-js-yaml](https://atom.io/packages/linter-js-yaml)
  * Docs
    * [dash](https://atom.io/packages/dash)
    * [Hyperclick](https://atom.io/packages/hyperclick), [js-hyperclick](https://atom.io/packages/js-hyperclick)
    * [keybinding-cheatsheet](https://atom.io/packages/keybinding-cheatsheet)
  * Assistant
    * [Project Manager](https://atom.io/packages/project-manager)
    * [todo-show](https://atom.io/packages/todo-show) / [imdone-atom](https://atom.io/packages/imdone-atom)
  * Integration
    * [GitHub for Atom](https://github.atom.io/)
    * [Build](https://atom.io/packages/build)
      * [AtomBuild](https://atombuild.github.io/)
    * [Markdown Preview Plus](https://atom.io/packages/markdown-preview-plus)
* Out-of-the-box Atom IDE
  * [YAtom](https://github.com/dexteryy/YAtom) (author's own project)
  * [Nuclide](https://nuclide.io/)
  * [Reactide](http://reactide.io/)
* Other Electron-based IDE
  * [Deco](https://www.decoide.org/)
* [WebStorm](https://www.jetbrains.com/webstorm/)
* Programming Fonts
  * [Hack](http://sourcefoundry.org/hack/)
  * [Anonymous Pro](https://www.marksimonson.com/fonts/view/anonymous-pro)
  * [Source Code Pro](http://adobe-fonts.github.io/source-code-pro/)
  * [Fira Mono](http://mozilla.github.io/Fira/)
  * [Google Noto Mono](https://www.google.com/get/noto/)
  * [Droid Sans Mono](https://fonts.google.com/specimen/Droid+Sans+Mono)
  * [Space Mono](https://fonts.google.com/specimen/Space%20Mono)
  * [M+](http://mplus-fonts.osdn.jp/about-en.html)
  * [Mononoki](http://madmalik.github.io/mononoki/)
  * [Profont](http://tobiasjung.name/profont/)

\>\> Return to [Table of Contents](#table-of-contents)

### Useful Apps

* Playground
  * [CodePen](http://codepen.io/) / [CodeSandbox](https://codesandbox.io/)
    * CDN for npm - [unpkg](https://unpkg.com/)
  * [RunKit](https://runkit.com)
  * [RequestBin](https://requestbin.com/)
  * [jsPerf](https://jsperf.com/)
  * [CSS in JS Playground](https://css-in-js-playground.com/)
  * [GraphQL Playground](https://github.com/graphcool/graphql-playground), [Apollo Launchpad](https://launchpad.graphql.com)
  * [GLSL Sandbox](http://glslsandbox.com/)
  * [ImmutableJS REPL](http://neilff.github.io/immutable-repl/?)
* Visual Tools
  * Performance
    * [Cuzillion](http://stevesouders.com/cuzillion/)
    * [Critical Path CSS Generator](https://jonassebastianohlsson.com/criticalpathcssgenerator/)
  * CSS
    * [cssreference.io](http://cssreference.io/)
    * [EnjoyCSS](http://enjoycss.com/)
    * Easing - [cubic-bezier](http://cubic-bezier.com/) / [Ceaser CSS Easing Animation Tool](https://matthewlein.com/ceaser/) / [Custom easing functions](http://www.joelambert.co.uk/morf/) / [Easing functions](http://easings.net/)
    * Flexbox - [Fibonacci Flexbox Composer](http://maxsteenbergen.com/fibonacci/) / [CSS Flexbox Please!](https://demo.agektmr.com/flexbox/) / [Flexy Boxes](http://the-echoplex.net/flexyboxes/) / [Flexbox Playground](https://demos.scotch.io/visual-guide-to-css3-flexbox-flexbox-playground/demos/) / [flexplorer](http://bennettfeely.com/flexplorer/)
    * Animation - [CSS3 Keyframes Animation Generator](http://cssanimate.com/) / [Mantra](http://jeremyckahn.github.io/mantra/) / [Bounce.js](http://bouncejs.com/)
    * Gradient - [Ultimate CSS Gradient Generator](http://www.colorzilla.com/gradient-editor/)
    * [Quantity Queries Builder](http://quantityqueries.com/)
    * Shapes - [CSS triangle generator](http://apps.eky.hk/css-triangle-generator/),  [Tridiv CSS 3D Editor](http://tridiv.com/)
    * [HTML Table Generator](http://www.tablesgenerator.com/html_tables)
  * JS
    * [Keyboard Event Viewer](https://w3c.github.io/uievents/tools/key-event-viewer.html)
    * [Web Audio Playground](http://webaudioplayground.appspot.com/)
    * [Regex101](https://regex101.com/) / [Debuggex](https://www.debuggex.com/)
* Viewer
  * [JSON Viewer](https://github.com/tulios/json-viewer), [XML Tree](https://chrome.google.com/webstore/detail/xml-tree/gbammbheopgpmaagmckhpjbfgdfkpadb)
  * [JS Nice](http://www.jsnice.org/) / [JS Beautifier](http://jsbeautifier.org/)
  * [GraphQL Voyager](https://apis.guru/graphql-voyager/), [GraphQL Docs](https://graphql-docs.com/), [GraphQL Visualizer / graphqlviz](http://nathanrandal.com/graphql-visualizer/) / [graphqlviz](https://github.com/sheerun/graphqlviz)
  * [AST Explorer](http://astexplorer.net/)
  * [DevTools Timeline Viewer](https://chromedevtools.github.io/timeline-viewer/)
  * [Text Escaping and Unescaping in JavaScript](http://0xcc.net/jsescape/)
  * [HTML Entity Lookup](http://entity-lookup.leftlogic.com/) / [HTML Arrows](https://www.toptal.com/designers/htmlarrows/)
* Docs
  * [Dash](https://kapeli.com/dash) / [DevDocs](http://devdocs.io/) / [Velocity](https://velocity.silverlakesoftware.com/) / [Zeal](https://zealdocs.org/)
* Automation
  * [RobotJS](https://robotjs.io/)

\>\> Return to [Table of Contents](#table-of-contents)

### Collaboration

* Version Control
  * Workflow
    * [Comparing Workflows](https://www.atlassian.com/git/tutorials/comparing-workflows)
    * [Understanding the GitHub Flow](https://guides.github.com/introduction/flow/)
    * [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/)
  * GUI
    * [SourceTree](https://www.sourcetreeapp.com/)
  * Github
    * [GitHub Cheat Sheet](https://github.com/tiimgreen/github-cheat-sheet)
    * [Github Help](https://help.github.com/)
    * [How we organize GitHub issues: A simple styleguide for tagging](https://robinpowered.com/blog/best-practice-system-for-organizing-and-tagging-github-issues/)
    * Chrome Extensions
      * [Chrome Extensions](Topics/Chrome%20Extensions.md)
* ChatOps
  * [What is ChatOps? And How do I Get Started?](https://www.pagerduty.com/blog/what-is-chatops/), \
    [What is ChatOps? A guide to its evolution, adoption, and significance](https://www.atlassian.com/blog/software-teams/what-is-chatops-adoption-guide)
  * [Hubot](https://hubot.github.com/)
    * Adapters - [Slack](https://github.com/slackapi/hubot-slack) / [Discord](http://npmjs.com/package/hubot-discord) / [IRC](https://www.npmjs.com/package/hubot-irc) / [Wechat](https://www.npmjs.com/package/hubot-weixin) / [QQ](https://www.npmjs.com/package/hubot-qq)
* Kanban
  * What is Kanban? - [A](https://leankit.com/learn/kanban/what-is-kanban/), [B](http://kanbanblog.com/explained/)
  * [Getting Started With Trello](https://trello.com/guide)
  * [Github Project Boards](https://help.github.com/articles/tracking-the-progress-of-your-work-with-project-boards/)
* Presentation
  * Markdown
    * [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
    * [Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax)
  * Diagram
    * [Mermaid](https://mermaidjs.github.io/)
      * [Mermaid Live Editor](https://mermaidjs.github.io/mermaid-live-editor/)
  * Slides
    * [Remark](https://github.com/gnab/remark)
      * [remarker](https://github.com/kt3k/remarker)
* Design
  * [Sketch](https://www.sketchapp.com/learn/) / [Figma](https://www.figma.com/)
  * [InVision](https://www.invisionapp.com/) / [Atomic](https://atomic.io/) / [Proto.io](https://proto.io/)
  * [Zeplin](https://zeplin.io/) / [Sympli](https://sympli.io/) / [Avocode](https://avocode.com/)
  * [After Effects](http://www.adobe.com/products/aftereffects.html) + [Lottie](https://airbnb.design/lottie/) / [bodymovin](https://github.com/bodymovin/bodymovin) / [Inspector Spacetime](https://google.github.io/inspectorspacetime/) + [Sketch2AE](https://google.github.io/sketch2ae/)

---

### [Lists-Index](Links/Lists%20/Lists-Index.md)