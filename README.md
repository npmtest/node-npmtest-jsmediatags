# npmtest-jsmediatags

#### basic test coverage for  [jsmediatags (v3.4.0)](https://github.com/aadsm/jsmediatags#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-jsmediatags.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-jsmediatags) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-jsmediatags.svg)](https://travis-ci.org/npmtest/node-npmtest-jsmediatags)

#### Media Tags Reader (ID3, MP4)

[![NPM](https://nodei.co/npm/jsmediatags.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/jsmediatags)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-jsmediatags/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-jsmediatags/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-jsmediatags/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-jsmediatags/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-jsmediatags/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-jsmediatags/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-jsmediatags/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-jsmediatags/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-jsmediatags/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-jsmediatags/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-jsmediatags/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-jsmediatags/build/test-report.html](https://npmtest.github.io/node-npmtest-jsmediatags/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-jsmediatags/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-jsmediatags/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-jsmediatags/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-jsmediatags/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-jsmediatags/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-jsmediatags/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-jsmediatags/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-jsmediatags/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "jsmediatags",
    "version": "3.4.0",
    "description": "Media Tags Reader (ID3, MP4)",
    "author": {
        "name": "António Afonso"
    },
    "contributors": [
        {
            "name": "Jacob Seidelin"
        },
        {
            "name": "Joshua Kifer"
        },
        {
            "name": "Jesse Ditson"
        }
    ],
    "main": "build2/jsmediatags.js",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/aadsm/jsmediatags.git"
    },
    "keywords": [
        "ID3",
        "tags",
        "mp3",
        "audio",
        "mp4"
    ],
    "license": "BSD-3-Clause",
    "bugs": {
        "url": "https://github.com/aadsm/jsmediatags/issues"
    },
    "homepage": "https://github.com/aadsm/jsmediatags#readme",
    "dependencies": {
        "xhr2": "~0.1.3"
    },
    "devDependencies": {
        "babel-plugin-transform-flow-strip-types": "~6.7.0",
        "babel-plugin-transform-es2015-modules-commonjs": "~6.7.4",
        "babel-plugin-transform-es2015-classes": "~6.6.5",
        "babel-plugin-transform-es2015-block-scoping": "~6.7.1",
        "babel-plugin-transform-class-properties": "~6.6.0",
        "babel-jest": "~12.0.2",
        "babel-core": "~6.7.7",
        "babel-cli": "~6.7.7",
        "jest-cli": "~12.0.2",
        "browserify": "~13.0.0",
        "watchify": "~3.7.0",
        "babelify": "~7.3.0",
        "google-closure-compiler": "20160315.2.0"
    },
    "scripts": {
        "test": "jest",
        "build": "babel src --ignore __tests__,__mocks,FlowTypes.js --out-dir build2",
        "watch": "babel --ignore __tests__,__mocks,FlowTypes.js --watch src --out-dir build2",
        "dist-dev": "mkdir -p dist && browserify src/jsmediatags.js --detect-globals false -i ./src/NodeFileReader.js -o dist/jsmediatags.js -s jsmediatags -t [ babelify --plugins [ transform-flow-strip-types transform-es2015-modules-commonjs transform-class-properties transform-es2015-classes transform-es2015-block-scoping ] ]",
        "dist-watch": "mkdir -p dist && watchify src/jsmediatags.js -v --detect-globals false -i ./src/NodeFileReader.js -o dist/jsmediatags.js -s jsmediatags -t [ babelify --plugins [ transform-flow-strip-types transform-es2015-modules-commonjs transform-class-properties transform-es2015-classes transform-es2015-block-scoping ] ]",
        "dist": "npm run dist-dev && java -jar node_modules/google-closure-compiler/compiler.jar --warning_level QUIET --compilation_level SIMPLE_OPTIMIZATIONS --js dist/jsmediatags.js > dist/jsmediatags.min.js"
    },
    "jest": {
        "rootDir": "./src",
        "scriptPreprocessor": "../node_modules/babel-jest"
    },
    "engines": {
        "node": ">=4.0.0"
    },
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
