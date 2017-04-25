# npmdoc-chokidar

#### basic api documentation for  [chokidar (v1.6.1)](https://github.com/paulmillr/chokidar)  [![npm package](https://img.shields.io/npm/v/npmdoc-chokidar.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-chokidar) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-chokidar.svg)](https://travis-ci.org/npmdoc/node-npmdoc-chokidar)

#### A neat wrapper around node.js fs.watch / fs.watchFile / fsevents.

[![NPM](https://nodei.co/npm/chokidar.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/chokidar)

- [https://npmdoc.github.io/node-npmdoc-chokidar/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-chokidar/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-chokidar/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-chokidar/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-chokidar/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-chokidar/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Paul Miller",
        "url": "http://paulmillr.com"
    },
    "bugs": {
        "url": "http://github.com/paulmillr/chokidar/issues"
    },
    "dependencies": {
        "anymatch": "^1.3.0",
        "async-each": "^1.0.0",
        "fsevents": "^1.0.0",
        "glob-parent": "^2.0.0",
        "inherits": "^2.0.1",
        "is-binary-path": "^1.0.0",
        "is-glob": "^2.0.0",
        "path-is-absolute": "^1.0.0",
        "readdirp": "^2.0.0"
    },
    "description": "A neat wrapper around node.js fs.watch / fs.watchFile / fsevents.",
    "devDependencies": {
        "chai": "^3.2.0",
        "coveralls": "^2.11.2",
        "graceful-fs": "4.1.4",
        "istanbul": "^0.3.20",
        "mocha": "^2.0.0",
        "rimraf": "^2.4.3",
        "sinon": "^1.10.3",
        "sinon-chai": "^2.6.0"
    },
    "directories": {},
    "dist": {
        "shasum": "2f4447ab5e96e50fb3d789fd90d4c72e0e4c70c2",
        "tarball": "https://registry.npmjs.org/chokidar/-/chokidar-1.6.1.tgz"
    },
    "files": [
        "index.js",
        "lib/"
    ],
    "gitHead": "c08145c5368fac6441773e621da9db215cc0d3b2",
    "homepage": "https://github.com/paulmillr/chokidar",
    "keywords": [
        "fs",
        "watch",
        "watchFile",
        "watcher",
        "watching",
        "file",
        "fsevents"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "paulmillr"
        },
        {
            "name": "es128"
        }
    ],
    "name": "chokidar",
    "optionalDependencies": {
        "fsevents": "^1.0.0"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/paulmillr/chokidar.git"
    },
    "scripts": {
        "ci-test": "istanbul cover _mocha && cat ./coverage/lcov.info | coveralls",
        "test": "istanbul test node_modules/mocha/bin/_mocha"
    },
    "version": "1.6.1",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
