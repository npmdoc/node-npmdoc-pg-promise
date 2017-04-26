# npmdoc-pg-promise

#### basic api documentation for  [pg-promise (v5.6.7)](https://github.com/vitaly-t/pg-promise)  [![npm package](https://img.shields.io/npm/v/npmdoc-pg-promise.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-pg-promise) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-pg-promise.svg)](https://travis-ci.org/npmdoc/node-npmdoc-pg-promise)

#### Promises interface for PostgreSQL

[![NPM](https://nodei.co/npm/pg-promise.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/pg-promise)

- [https://npmdoc.github.io/node-npmdoc-pg-promise/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-pg-promise/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-pg-promise/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-pg-promise/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-pg-promise/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-pg-promise/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Vitaly Tomilov"
    },
    "bugs": {
        "url": "https://github.com/vitaly-t/pg-promise/issues"
    },
    "dependencies": {
        "manakin": "0.4",
        "pg": "5.1",
        "pg-minify": "0.4",
        "spex": "1.2"
    },
    "description": "Promises interface for PostgreSQL",
    "devDependencies": {
        "@types/node": "6.x",
        "JSONStream": "1.x",
        "bluebird": "3.x",
        "coveralls": "2.11",
        "eslint": "3.x",
        "istanbul": "0.4",
        "jasmine-node": "1.x",
        "jsdoc": "3.x",
        "pg-query-stream": "1.x",
        "typescript": "2.x"
    },
    "directories": {},
    "dist": {
        "shasum": "e5700066d0b711957e5224b1039b14ddb12df54a",
        "tarball": "https://registry.npmjs.org/pg-promise/-/pg-promise-5.6.7.tgz"
    },
    "engines": {
        "node": ">=4.0",
        "npm": ">=2.15"
    },
    "files": [
        "lib",
        "typescript"
    ],
    "gitHead": "19ec2930a40efd7c66157fb781ec3b319028165a",
    "homepage": "https://github.com/vitaly-t/pg-promise",
    "keywords": [
        "pg",
        "promise",
        "postgres"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "vitaly.tomilov"
        }
    ],
    "name": "pg-promise",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/vitaly-t/pg-promise.git"
    },
    "scripts": {
        "coverage": "istanbul cover ./node_modules/jasmine-node/bin/jasmine-node test",
        "doc": "jsdoc -c ./jsdoc/jsDoc.json ./jsdoc/README.md",
        "lint": "eslint ./lib",
        "test": "jasmine-node test",
        "test-native": "jasmine-node test --config PG_NATIVE true",
        "travis": "npm run lint && istanbul cover ./node_modules/jasmine-node/bin/jasmine-node test --captureExceptions && cat ./coverage/lcov.info | ./node_modules/coveralls/bin/coveralls.js && rm -rf ./coverage"
    },
    "typings": "typescript/pg-promise.d.ts",
    "version": "5.6.7",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
