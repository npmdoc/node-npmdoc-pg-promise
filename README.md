# api documentation for  [pg-promise (v5.6.4)](https://github.com/vitaly-t/pg-promise)  [![npm package](https://img.shields.io/npm/v/npmdoc-pg-promise.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-pg-promise) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-pg-promise.svg)](https://travis-ci.org/npmdoc/node-npmdoc-pg-promise)
#### Promises interface for PostgreSQL

[![NPM](https://nodei.co/npm/pg-promise.png?downloads=true)](https://www.npmjs.com/package/pg-promise)

[![apidoc](https://npmdoc.github.io/node-npmdoc-pg-promise/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-pg-promise_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-pg-promise/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-pg-promise/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-pg-promise/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Vitaly Tomilov",
        "email": "vitaly.tomilov@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/vitaly-t/pg-promise/issues",
        "email": "vitaly.tomilov@gmail.com"
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
        "shasum": "80b18a2a1bdd9af7fb0087e01a1b87ada8559a71",
        "tarball": "https://registry.npmjs.org/pg-promise/-/pg-promise-5.6.4.tgz"
    },
    "engines": {
        "node": ">=4.0",
        "npm": ">=2.15"
    },
    "files": [
        "lib",
        "typescript"
    ],
    "gitHead": "2e381403ff346114e169884e6ab8613989cb5356",
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
            "name": "vitaly.tomilov",
            "email": "vitaly.tomilov@gmail.com"
        }
    ],
    "name": "pg-promise",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "5.6.4"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module pg-promise](#apidoc.module.pg-promise)
1.  [function <span class="apidocSignatureSpan">pg-promise.</span>ParameterizedQuery (text, values)](#apidoc.element.pg-promise.ParameterizedQuery)
1.  [function <span class="apidocSignatureSpan">pg-promise.</span>PreparedStatement (name, text, values)](#apidoc.element.pg-promise.PreparedStatement)
1.  [function <span class="apidocSignatureSpan">pg-promise.</span>PromiseAdapter (create, resolve, reject)](#apidoc.element.pg-promise.PromiseAdapter)
1.  [function <span class="apidocSignatureSpan">pg-promise.</span>QueryFile (file, options)](#apidoc.element.pg-promise.QueryFile)
1.  [function <span class="apidocSignatureSpan">pg-promise.</span>errors.ParameterizedQueryError (error, ps)](#apidoc.element.pg-promise.errors.ParameterizedQueryError)
1.  [function <span class="apidocSignatureSpan">pg-promise.</span>errors.PreparedStatementError (error, ps)](#apidoc.element.pg-promise.errors.PreparedStatementError)
1.  [function <span class="apidocSignatureSpan">pg-promise.</span>errors.QueryFileError (error, qf)](#apidoc.element.pg-promise.errors.QueryFileError)
1.  [function <span class="apidocSignatureSpan">pg-promise.</span>errors.QueryResultError (code, result, query, values)](#apidoc.element.pg-promise.errors.QueryResultError)
1.  [function <span class="apidocSignatureSpan">pg-promise.</span>minify (sql, options)](#apidoc.element.pg-promise.minify)
1.  [function <span class="apidocSignatureSpan">pg-promise.</span>minify.SQLParsingError (code, position)](#apidoc.element.pg-promise.minify.SQLParsingError)
1.  object <span class="apidocSignatureSpan">pg-promise.</span>ParameterizedQuery.prototype
1.  object <span class="apidocSignatureSpan">pg-promise.</span>PreparedStatement.prototype
1.  object <span class="apidocSignatureSpan">pg-promise.</span>QueryFile.prototype
1.  object <span class="apidocSignatureSpan">pg-promise.</span>array
1.  object <span class="apidocSignatureSpan">pg-promise.</span>as
1.  object <span class="apidocSignatureSpan">pg-promise.</span>errors
1.  object <span class="apidocSignatureSpan">pg-promise.</span>errors.ParameterizedQueryError.prototype
1.  object <span class="apidocSignatureSpan">pg-promise.</span>errors.PreparedStatementError.prototype
1.  object <span class="apidocSignatureSpan">pg-promise.</span>errors.QueryFileError.prototype
1.  object <span class="apidocSignatureSpan">pg-promise.</span>errors.QueryResultError.prototype
1.  object <span class="apidocSignatureSpan">pg-promise.</span>events
1.  object <span class="apidocSignatureSpan">pg-promise.</span>formatting
1.  object <span class="apidocSignatureSpan">pg-promise.</span>minify.SQLParsingError.prototype
1.  object <span class="apidocSignatureSpan">pg-promise.</span>queryResult
1.  object <span class="apidocSignatureSpan">pg-promise.</span>special
1.  object <span class="apidocSignatureSpan">pg-promise.</span>txMode
1.  object <span class="apidocSignatureSpan">pg-promise.</span>utils

#### [module pg-promise.ParameterizedQuery](#apidoc.module.pg-promise.ParameterizedQuery)
1.  [function <span class="apidocSignatureSpan">pg-promise.</span>ParameterizedQuery (text, values)](#apidoc.element.pg-promise.ParameterizedQuery.ParameterizedQuery)

#### [module pg-promise.ParameterizedQuery.prototype](#apidoc.module.pg-promise.ParameterizedQuery.prototype)
1.  [function <span class="apidocSignatureSpan">pg-promise.ParameterizedQuery.prototype.</span>toString (level)](#apidoc.element.pg-promise.ParameterizedQuery.prototype.toString)

#### [module pg-promise.PreparedStatement](#apidoc.module.pg-promise.PreparedStatement)
1.  [function <span class="apidocSignatureSpan">pg-promise.</span>PreparedStatement (name, text, values)](#apidoc.element.pg-promise.PreparedStatement.PreparedStatement)

#### [module pg-promise.PreparedStatement.prototype](#apidoc.module.pg-promise.PreparedStatement.prototype)
1.  [function <span class="apidocSignatureSpan">pg-promise.PreparedStatement.prototype.</span>toString (level)](#apidoc.element.pg-promise.PreparedStatement.prototype.toString)

#### [module pg-promise.QueryFile](#apidoc.module.pg-promise.QueryFile)
1.  [function <span class="apidocSignatureSpan">pg-promise.</span>QueryFile (file, options)](#apidoc.element.pg-promise.QueryFile.QueryFile)

#### [module pg-promise.QueryFile.prototype](#apidoc.module.pg-promise.QueryFile.prototype)
1.  [function <span class="apidocSignatureSpan">pg-promise.QueryFile.prototype.</span>inspect ()](#apidoc.element.pg-promise.QueryFile.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">pg-promise.QueryFile.prototype.</span>toString (level)](#apidoc.element.pg-promise.QueryFile.prototype.toString)

#### [module pg-promise.array](#apidoc.module.pg-promise.array)
1.  [function <span class="apidocSignatureSpan">pg-promise.array.</span>countIf (arr, cb, obj)](#apidoc.element.pg-promise.array.countIf)
1.  [function <span class="apidocSignatureSpan">pg-promise.array.</span>filter (arr, cb, obj)](#apidoc.element.pg-promise.array.filter)
1.  [function <span class="apidocSignatureSpan">pg-promise.array.</span>forEach (arr, cb, obj)](#apidoc.element.pg-promise.array.forEach)
1.  [function <span class="apidocSignatureSpan">pg-promise.array.</span>map (arr, cb, obj)](#apidoc.element.pg-promise.array.map)

#### [module pg-promise.as](#apidoc.module.pg-promise.as)
1.  [function <span class="apidocSignatureSpan">pg-promise.as.</span>array (arr)](#apidoc.element.pg-promise.as.array)
1.  [function <span class="apidocSignatureSpan">pg-promise.as.</span>bool (value)](#apidoc.element.pg-promise.as.bool)
1.  [function <span class="apidocSignatureSpan">pg-promise.as.</span>buffer (obj, raw)](#apidoc.element.pg-promise.as.buffer)
1.  [function <span class="apidocSignatureSpan">pg-promise.as.</span>csv (resolveFunc(values)](#apidoc.element.pg-promise.as.csv)
1.  [function <span class="apidocSignatureSpan">pg-promise.as.</span>date (d, raw)](#apidoc.element.pg-promise.as.date)
1.  [function <span class="apidocSignatureSpan">pg-promise.as.</span>format (query, values, options)](#apidoc.element.pg-promise.as.format)
1.  [function <span class="apidocSignatureSpan">pg-promise.as.</span>func (func, raw, obj)](#apidoc.element.pg-promise.as.func)
1.  [function <span class="apidocSignatureSpan">pg-promise.as.</span>json (obj, raw)](#apidoc.element.pg-promise.as.json)
1.  [function <span class="apidocSignatureSpan">pg-promise.as.</span>name (name)](#apidoc.element.pg-promise.as.name)
1.  [function <span class="apidocSignatureSpan">pg-promise.as.</span>number (num)](#apidoc.element.pg-promise.as.number)
1.  [function <span class="apidocSignatureSpan">pg-promise.as.</span>text (value, raw)](#apidoc.element.pg-promise.as.text)
1.  [function <span class="apidocSignatureSpan">pg-promise.as.</span>value (value)](#apidoc.element.pg-promise.as.value)

#### [module pg-promise.errors](#apidoc.module.pg-promise.errors)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.</span>ParameterizedQueryError (error, ps)](#apidoc.element.pg-promise.errors.ParameterizedQueryError)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.</span>PreparedStatementError (error, ps)](#apidoc.element.pg-promise.errors.PreparedStatementError)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.</span>QueryFileError (error, qf)](#apidoc.element.pg-promise.errors.QueryFileError)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.</span>QueryResultError (code, result, query, values)](#apidoc.element.pg-promise.errors.QueryResultError)
1.  object <span class="apidocSignatureSpan">pg-promise.errors.</span>queryResultErrorCode

#### [module pg-promise.errors.ParameterizedQueryError](#apidoc.module.pg-promise.errors.ParameterizedQueryError)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.</span>ParameterizedQueryError (error, ps)](#apidoc.element.pg-promise.errors.ParameterizedQueryError.ParameterizedQueryError)

#### [module pg-promise.errors.ParameterizedQueryError.prototype](#apidoc.module.pg-promise.errors.ParameterizedQueryError.prototype)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.ParameterizedQueryError.prototype.</span>inspect ()](#apidoc.element.pg-promise.errors.ParameterizedQueryError.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.ParameterizedQueryError.prototype.</span>toString (level)](#apidoc.element.pg-promise.errors.ParameterizedQueryError.prototype.toString)

#### [module pg-promise.errors.PreparedStatementError](#apidoc.module.pg-promise.errors.PreparedStatementError)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.</span>PreparedStatementError (error, ps)](#apidoc.element.pg-promise.errors.PreparedStatementError.PreparedStatementError)

#### [module pg-promise.errors.PreparedStatementError.prototype](#apidoc.module.pg-promise.errors.PreparedStatementError.prototype)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.PreparedStatementError.prototype.</span>inspect ()](#apidoc.element.pg-promise.errors.PreparedStatementError.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.PreparedStatementError.prototype.</span>toString (level)](#apidoc.element.pg-promise.errors.PreparedStatementError.prototype.toString)

#### [module pg-promise.errors.QueryFileError](#apidoc.module.pg-promise.errors.QueryFileError)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.</span>QueryFileError (error, qf)](#apidoc.element.pg-promise.errors.QueryFileError.QueryFileError)

#### [module pg-promise.errors.QueryFileError.prototype](#apidoc.module.pg-promise.errors.QueryFileError.prototype)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.QueryFileError.prototype.</span>inspect ()](#apidoc.element.pg-promise.errors.QueryFileError.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.QueryFileError.prototype.</span>toString (level)](#apidoc.element.pg-promise.errors.QueryFileError.prototype.toString)

#### [module pg-promise.errors.QueryResultError](#apidoc.module.pg-promise.errors.QueryResultError)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.</span>QueryResultError (code, result, query, values)](#apidoc.element.pg-promise.errors.QueryResultError.QueryResultError)

#### [module pg-promise.errors.QueryResultError.prototype](#apidoc.module.pg-promise.errors.QueryResultError.prototype)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.QueryResultError.prototype.</span>inspect ()](#apidoc.element.pg-promise.errors.QueryResultError.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">pg-promise.errors.QueryResultError.prototype.</span>toString (level)](#apidoc.element.pg-promise.errors.QueryResultError.prototype.toString)

#### [module pg-promise.events](#apidoc.module.pg-promise.events)
1.  [function <span class="apidocSignatureSpan">pg-promise.events.</span>connect (ctx, client, isFresh)](#apidoc.element.pg-promise.events.connect)
1.  [function <span class="apidocSignatureSpan">pg-promise.events.</span>disconnect (ctx, client)](#apidoc.element.pg-promise.events.disconnect)
1.  [function <span class="apidocSignatureSpan">pg-promise.events.</span>error (options, err, context)](#apidoc.element.pg-promise.events.error)
1.  [function <span class="apidocSignatureSpan">pg-promise.events.</span>extend (options, obj, dc)](#apidoc.element.pg-promise.events.extend)
1.  [function <span class="apidocSignatureSpan">pg-promise.events.</span>query (options, context)](#apidoc.element.pg-promise.events.query)
1.  [function <span class="apidocSignatureSpan">pg-promise.events.</span>receive (options, data, result, context)](#apidoc.element.pg-promise.events.receive)
1.  [function <span class="apidocSignatureSpan">pg-promise.events.</span>task (options, context)](#apidoc.element.pg-promise.events.task)
1.  [function <span class="apidocSignatureSpan">pg-promise.events.</span>transact (options, context)](#apidoc.element.pg-promise.events.transact)
1.  [function <span class="apidocSignatureSpan">pg-promise.events.</span>unexpected (event, e)](#apidoc.element.pg-promise.events.unexpected)

#### [module pg-promise.formatting](#apidoc.module.pg-promise.formatting)
1.  [function <span class="apidocSignatureSpan">pg-promise.formatting.</span>formatFunction (funcName, values, capSQL)](#apidoc.element.pg-promise.formatting.formatFunction)
1.  [function <span class="apidocSignatureSpan">pg-promise.formatting.</span>formatQuery (query, values, raw, options)](#apidoc.element.pg-promise.formatting.formatQuery)
1.  object <span class="apidocSignatureSpan">pg-promise.formatting.</span>as

#### [module pg-promise.minify](#apidoc.module.pg-promise.minify)
1.  [function <span class="apidocSignatureSpan">pg-promise.</span>minify (sql, options)](#apidoc.element.pg-promise.minify.minify)
1.  [function <span class="apidocSignatureSpan">pg-promise.minify.</span>SQLParsingError (code, position)](#apidoc.element.pg-promise.minify.SQLParsingError)
1.  object <span class="apidocSignatureSpan">pg-promise.minify.</span>parsingErrorCode

#### [module pg-promise.minify.SQLParsingError](#apidoc.module.pg-promise.minify.SQLParsingError)
1.  [function <span class="apidocSignatureSpan">pg-promise.minify.</span>SQLParsingError (code, position)](#apidoc.element.pg-promise.minify.SQLParsingError.SQLParsingError)

#### [module pg-promise.minify.SQLParsingError.prototype](#apidoc.module.pg-promise.minify.SQLParsingError.prototype)
1.  [function <span class="apidocSignatureSpan">pg-promise.minify.SQLParsingError.prototype.</span>inspect ()](#apidoc.element.pg-promise.minify.SQLParsingError.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">pg-promise.minify.SQLParsingError.prototype.</span>toString (level)](#apidoc.element.pg-promise.minify.SQLParsingError.prototype.toString)

#### [module pg-promise.special](#apidoc.module.pg-promise.special)
1.  [function <span class="apidocSignatureSpan">pg-promise.special.</span>SpecialQuery (type)](#apidoc.element.pg-promise.special.SpecialQuery)
1.  object <span class="apidocSignatureSpan">pg-promise.special.</span>cache

#### [module pg-promise.txMode](#apidoc.module.pg-promise.txMode)
1.  [function <span class="apidocSignatureSpan">pg-promise.txMode.</span>TransactionMode (tiLevel, readOnly, deferrable)](#apidoc.element.pg-promise.txMode.TransactionMode)
1.  object <span class="apidocSignatureSpan">pg-promise.txMode.</span>isolationLevel

#### [module pg-promise.utils](#apidoc.module.pg-promise.utils)
1.  [function <span class="apidocSignatureSpan">pg-promise.utils.</span>buildSqlModule (config)](#apidoc.element.pg-promise.utils.buildSqlModule)
1.  [function <span class="apidocSignatureSpan">pg-promise.utils.</span>camelize (text)](#apidoc.element.pg-promise.utils.camelize)
1.  [function <span class="apidocSignatureSpan">pg-promise.utils.</span>camelizeVar (text)](#apidoc.element.pg-promise.utils.camelizeVar)
1.  [function <span class="apidocSignatureSpan">pg-promise.utils.</span>enumSql (dir, options, cb)](#apidoc.element.pg-promise.utils.enumSql)
1.  [function <span class="apidocSignatureSpan">pg-promise.utils.</span>objectToCode (obj, cb)](#apidoc.element.pg-promise.utils.objectToCode)



# <a name="apidoc.module.pg-promise"></a>[module pg-promise](#apidoc.module.pg-promise)

#### <a name="apidoc.element.pg-promise.ParameterizedQuery"></a>[function <span class="apidocSignatureSpan">pg-promise.</span>ParameterizedQuery (text, values)](#apidoc.element.pg-promise.ParameterizedQuery)
- description and source-code
```javascript
function ParameterizedQuery(text, values) {
    if (!(this instanceof ParameterizedQuery)) {
        return new ParameterizedQuery(text, values);
    }

    var currentError, PQ = {}, changed = true, state = {
        text: text,
        binary: undefined,
        rowMode: undefined
    };

    function setValues(v) {
        if (Array.isArray(v)) {
            if (v.length) {
                PQ.values = v;
            } else {
                delete PQ.values;
            }
        } else {
            if ($npm.utils.isNull(v)) {
                delete PQ.values;
            } else {
                PQ.values = [v];
            }
        }
    }

    setValues(values);

    /**
     * @name ParameterizedQuery#text
     * @type {string|QueryFile}
     * @description
     * A non-empty query string or a {@link QueryFile} object.
     */
    Object.defineProperty(this, 'text', {
        get: () => state.text,
        set: value => {
            if (value !== state.text) {
                state.text = value;
                changed = true;
            }
        }
    });

    /**
     * @name ParameterizedQuery#values
     * @type {array}
     * @description
     * Query formatting parameters, depending on the type:
     *
     * - 'null' / 'undefined' means the query has no formatting parameters
     * - 'Array' - it is an array of formatting parameters
     * - None of the above, means it is a single formatting value, which
     *   is then automatically wrapped into an array
     */
    Object.defineProperty(this, 'values', {
        get: () => PQ.values,
        set: value => {
            setValues(value);
        }
    });

    /**
     * @name ParameterizedQuery#binary
     * @type {boolean}
     * @default undefined
     * @description
     * Activates binary result mode. The default is the text mode.
     *
     * @see {@link http://www.postgresql.org/docs/devel/static/protocol-flow.html#PROTOCOL-FLOW-EXT-QUERY Extended Query}
     */
    Object.defineProperty(this, 'binary', {
        get: () => state.binary,
        set: value => {
            if (value !== state.binary) {
                state.binary = value;
                changed = true;
            }
        }
    });

    /**
     * @name ParameterizedQuery#rowMode
     * @type {string}
     * @default undefined
     * @description
     * Changes the way data arrives to the client, with only one value supported by $[pg]:
     *  - 'rowMode = 'array'' will make all data rows arrive as arrays of values.
     *    By default, rows arrive as objects.
     */
    Object.defineProperty(this, 'rowMode', {
        get: () => state.rowMode,
        set: value => {
            if (value !== state.rowMode) {
                state.rowMode = value;
                changed = true;
            }
        }
    });

    /**
     * @name ParameterizedQuery#error
     * @type {errors.ParameterizedQueryError}
     * @default undefined
     * @readonly
     * @description
     * When in an error state, it is set to a {@link errors.ParameterizedQueryError ParameterizedQueryError} object. Otherwise,
it is 'undefined'.
     *
     * This property is primarily for internal use by the library.
     */
    Object.defineProperty(this, 'error', {
        get: () => currentError
    });

    if ($npm.utils.isObject(text, ['text'])) {
        state.text = text.text;
        state.binary = text.binary;
        state.rowMode = text.rowMode;
        setValues(text.values);
    }

    /**
     * @method ParameterizedQuery.parse
     * @description
     * Parses the current object and returns a simple '{text, values}', if successful,
     * or else it returns a {@link errors.ParameterizedQueryError ParameterizedQueryError} object.
     *
     * This method is primarily for internal use by the library.
     *
     * @returns {{text, values}|errors.ParameterizedQueryError}
     */
    this.parse = () => {

        var qf = state.text instanceof $npm.QueryFile ? s ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.PreparedStatement"></a>[function <span class="apidocSignatureSpan">pg-promise.</span>PreparedStatement (name, text, values)](#apidoc.element.pg-promise.PreparedStatement)
- description and source-code
```javascript
function PreparedStatement(name, text, values) {
    if (!(this instanceof PreparedStatement)) {
        return new PreparedStatement(name, text, values);
    }

    var currentError, PS = {}, changed = true, state = {
        name: name,
        text: text,
        binary: undefined,
        rowMode: undefined,
        rows: undefined
    };

    function setValues(v) {
        if (Array.isArray(v)) {
            if (v.length) {
                PS.values = v;
            } else {
                delete PS.values;
            }
        } else {
            if ($npm.utils.isNull(v)) {
                delete PS.values;
            } else {
                PS.values = [v];
            }
        }
    }

    setValues(values);

    /**
     * @name PreparedStatement#name
     * @type {string}
     * @description
     * An arbitrary name given to this particular prepared statement. It must be unique within a single session and is
     * subsequently used to execute or deallocate a previously prepared statement.
     */
    Object.defineProperty(this, 'name', {
        get: () => state.name,
        set: value => {
            if (value !== state.name) {
                state.name = value;
                changed = true;
            }
        }
    });

    /**
     * @name PreparedStatement#text
     * @type {string|QueryFile}
     * @description
     * A non-empty query string or a {@link QueryFile} object.
     *
     * Changing this property for the same {@link PreparedStatement#name name} will have no effect, because queries
     * for Prepared Statements are cached, with {@link PreparedStatement#name name} being the cache key.
     */
    Object.defineProperty(this, 'text', {
        get: () => state.text,
        set: value => {
            if (value !== state.text) {
                state.text = value;
                changed = true;
            }
        }
    });

    /**
     * @name PreparedStatement#values
     * @type {array}
     * @description
     * Query formatting parameters, depending on the type:
     *
     * - 'null' / 'undefined' means the query has no formatting parameters
     * - 'Array' - it is an array of formatting parameters
     * - None of the above, means it is a single formatting value, which
     *   is then automatically wrapped into an array
     */
    Object.defineProperty(this, 'values', {
        get: () => PS.values,
        set: value => {
            setValues(value);
        }
    });

    /**
     * @name PreparedStatement#binary
     * @type {boolean}
     * @default undefined
     * @description
     * Activates binary result mode. The default is the text mode.
     *
     * @see {@link http://www.postgresql.org/docs/devel/static/protocol-flow.html#PROTOCOL-FLOW-EXT-QUERY Extended Query}
     */
    Object.defineProperty(this, 'binary', {
        get: () => state.binary,
        set: value => {
            if (value !== state.binary) {
                state.binary = value;
                changed = true;
            }
        }
    });

    /**
     * @name PreparedStatement#rowMode
     * @type {string}
     * @default undefined
     * @description
     * Changes the way data arrives to the client, with only one value supported by $[pg]:
     *  - 'rowMode = 'array'' will make all data rows arrive as arrays of values.
     *    By default, rows arrive as objects.
     */
    Object.defineProperty(this, 'rowMode', {
        get: () => state.rowMode,
        set: value => {
            if (value !== state.rowMode) {
                state.rowMode = value;
                changed = true;
            }
        }
    });

    /**
     * @name PreparedStatement#rows
     * @type {number}
     * @description
     * Number of rows to return at a time from a Prepared Statement's portal.
     * The default is 0, which means that all rows must be returned at once.
     */
    Object.defineProperty(this, 'rows', {
        get: () => state.rows,
        set: val ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.PromiseAdapter"></a>[function <span class="apidocSignatureSpan">pg-promise.</span>PromiseAdapter (create, resolve, reject)](#apidoc.element.pg-promise.PromiseAdapter)
- description and source-code
```javascript
function PromiseAdapter(create, resolve, reject) {

    if (!(this instanceof PromiseAdapter)) {
        return new PromiseAdapter(create, resolve, reject);
    }

    this.create = create;
    this.resolve = resolve;
    this.reject = reject;

    if (typeof create !== 'function') {
        throw new TypeError('Adapter requires a function to create a promise.');
    }

    if (typeof resolve !== 'function') {
        throw new TypeError('Adapter requires a function to resolve a promise.');
    }

    if (typeof reject !== 'function') {
        throw new TypeError('Adapter requires a function to reject a promise.');
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.QueryFile"></a>[function <span class="apidocSignatureSpan">pg-promise.</span>QueryFile (file, options)](#apidoc.element.pg-promise.QueryFile)
- description and source-code
```javascript
function QueryFile(file, options) {

    if (!(this instanceof QueryFile)) {
        return new QueryFile(file, options);
    }

    var sql, error, ready, modTime, after, filePath = file, opt = {
        debug: $npm.utils.isDev(),
        minify: false,
        compress: false
    };

    if (options && typeof options === 'object') {
        if (options.debug !== undefined) {
            opt.debug = !!options.debug;
        }
        if (options.minify !== undefined) {
            after = options.minify === 'after';
            opt.minify = after ? 'after' : !!options.minify;
        }
        if (options.compress !== undefined) {
            opt.compress = !!options.compress;
        }
        if (opt.compress && options.minify === undefined) {
            opt.minify = true;
        }
        if (options.params !== undefined) {
            opt.params = options.params;
        }
    }

    Object.freeze(opt);

    if ($npm.utils.isText(filePath) && !$npm.utils.isPathAbsolute(filePath)) {
        filePath = $npm.path.join($npm.utils.startDir, filePath);
    }

    // Custom Type Formatting support:
    this.formatDBType = function () {
        this.prepare(true);
        return this.query;
    };

    /**
     * @method QueryFile.prepare
     * @summary Prepares the query for execution.
     * @description
     * If the the query hasn't been prepared yet, it will read the file and process the contents according
     * to the parameters passed into the constructor.
     *
     * This method is primarily for internal use by the library.
     *
     * @param {boolean} [throwErrors=false]
     * Throw any error encountered.
     *
     */
    this.prepare = function (throwErrors) {
        var lastMod;
        if (opt.debug && ready) {
            try {
                lastMod = $npm.fs.statSync(filePath).mtime.getTime();
                if (lastMod === modTime) {
                    // istanbul ignore next;
                    // coverage for this works differently under Windows and Linux
                    return;
                }
                ready = false;
            } catch (e) {
                sql = undefined;
                ready = false;
                error = e;
                if (throwErrors) {
                    throw error;
                }
                return;
            }
        }
        if (ready) {
            return;
        }
        try {
            sql = $npm.fs.readFileSync(filePath, 'utf8');
            modTime = lastMod || $npm.fs.statSync(filePath).mtime.getTime();
            if (opt.minify && !after) {
                sql = $npm.minify(sql, {compress: opt.compress});
            }
            if (opt.params !== undefined) {
                sql = $npm.format(sql, opt.params, {partial: true});
            }
            if (opt.minify && after) {
                sql = $npm.minify(sql, {compress: opt.compress});
            }
            ready = true;
            error = undefined;
        } catch (e) {
            sql = undefined;
            error = new $npm.QueryFileError(e, this);
            if (throwErrors) {
                throw error;
            }
        }
    };

    /**
     * @name QueryFile#query
     * @type {string}
     * @default undefined
     * @readonly
     * @summary Prepared query string.
     * @description
     * When property {@link QueryFile#error error} is set, the query is 'undefined'.
     *
     * This property is primarily for internal use by the library.
     */
    Object.defineProperty(this, 'query', {
        get: () => sql
    });

    /**
     * @name QueryFile#error
     * @type {errors.QueryFileError}
     * @default undefined
     * @readonly
     * @description
     * When in an error state, it is set to a {@link errors.QueryFileError QueryFileError} object. Otherwise, it is 'undefined'.
     *
     * This property is primarily for internal use by the library.
     */
    Object.defineProperty(this, 'error', { ...
```
- example usage
```shell
...

Example:

'''js
// Helper for linking to external query files:
function sql(file) {
// consider using here: path.join(__dirname, file)
return new pgp.QueryFile(file, {minify: true});
}

// Create QueryFile globally, once per file:
var sqlFindUser = sql('./sql/findUser.sql');

db.one(sqlFindUser, {id: 123})
.then(user=> {
...
```

#### <a name="apidoc.element.pg-promise.errors.ParameterizedQueryError"></a>[function <span class="apidocSignatureSpan">pg-promise.</span>errors.ParameterizedQueryError (error, ps)](#apidoc.element.pg-promise.errors.ParameterizedQueryError)
- description and source-code
```javascript
function ParameterizedQueryError(error, ps) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'ParameterizedQueryError';
    this.stack = temp.stack;
    if (error instanceof $npm.QueryFileError) {
        this.error = error;
        this.message = 'Failed to initialize \'text\' from a QueryFile.';
    } else {
        this.message = error;
    }
    this.result = ps;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.errors.PreparedStatementError"></a>[function <span class="apidocSignatureSpan">pg-promise.</span>errors.PreparedStatementError (error, ps)](#apidoc.element.pg-promise.errors.PreparedStatementError)
- description and source-code
```javascript
function PreparedStatementError(error, ps) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'PreparedStatementError';
    this.stack = temp.stack;
    if (error instanceof $npm.QueryFileError) {
        this.error = error;
        this.message = 'Failed to initialize \'text\' from a QueryFile.';
    } else {
        this.message = error;
    }
    this.result = ps;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.errors.QueryFileError"></a>[function <span class="apidocSignatureSpan">pg-promise.</span>errors.QueryFileError (error, qf)](#apidoc.element.pg-promise.errors.QueryFileError)
- description and source-code
```javascript
function QueryFileError(error, qf) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'QueryFileError';
    this.stack = temp.stack;
    if (error instanceof $npm.minify.SQLParsingError) {
        this.error = error;
        this.message = 'Failed to parse the SQL.';
    } else {
        this.message = error.message;
    }
    this.file = qf.file;
    this.options = qf.options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.errors.QueryResultError"></a>[function <span class="apidocSignatureSpan">pg-promise.</span>errors.QueryResultError (code, result, query, values)](#apidoc.element.pg-promise.errors.QueryResultError)
- description and source-code
```javascript
function QueryResultError(code, result, query, values) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'QueryResultError';
    this.stack = temp.stack;
    this.message = errorMessages[code].message;
    this.code = code;
    this.result = result;
    this.query = query;
    this.values = values;
    this.received = result.rows.length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.minify"></a>[function <span class="apidocSignatureSpan">pg-promise.</span>minify (sql, options)](#apidoc.element.pg-promise.minify)
- description and source-code
```javascript
function minify(sql, options) {

    if (typeof sql !== 'string') {
        throw new TypeError("Input SQL must be a text string.");
    }

    if (options !== undefined && typeof options !== 'object') {
        throw new TypeError("Parameter 'options' must be an object.");
    }

    if (!sql.length) {
        return '';
    }

    var idx = 0, // current index
        result = '', // resulting sql
        len = sql.length, // sql length
        EOL = getEOL(sql), // end-of-line
        space = false, // add a space on the next step
        compress = options && options.compress; // option 'compress'

    do {
        var s = sql[idx], // current symbol;
            s1 = idx < len - 1 ? sql[idx + 1] : ''; // next symbol;

        if (isGap(s)) {
            while (++idx < len && isGap(sql[idx]));
            if (idx < len) {
                space = true;
            }
            idx--;
            continue;
        }

        if (s === '-' && s1 === '-') {
            var lb = sql.indexOf(EOL, idx + 2);
            if (lb < 0) {
                break;
            }
            idx = lb - 1;
            skipGaps();
            continue;
        }

        if (s === '/' && s1 === '*') {
            var end = sql.indexOf('*/', idx + 2);
            if (end < 0) {
                throwError(PEC.unclosedMLC);
            }
            idx = end + 1;
            skipGaps();
            continue;
        }

        if (s === '"') {
            var closeIdx = sql.indexOf('"', idx + 1);
            if (closeIdx < 0) {
                throwError(PEC.unclosedQI);
            }
            var text = sql.substr(idx, closeIdx - idx + 1);
            if (text.indexOf(EOL) > 0) {
                throwError(PEC.multiLineQI);
            }
            if (compress) {
                space = false;
            }
            addSpace();
            result += text;
            idx = closeIdx;
            skipGaps();
            continue;
        }

        if (s === '\'') {
            var closeIdx = idx;
            do {
                closeIdx = sql.indexOf('\'', closeIdx + 1);
                if (closeIdx > 0) {
                    var step = closeIdx;
                    while (++step < len && sql[step] === '\'');
                    if ((step - closeIdx) % 2) {
                        closeIdx = step - 1;
                        break;
                    }
                    closeIdx = step === len ? -1 : step;
                }
            } while (closeIdx > 0);
            if (closeIdx < 0) {
                throwError(PEC.unclosedText);
            }
            if (compress) {
                space = false;
            }
            addSpace();
            var text = sql.substr(idx, closeIdx - idx + 1);
            var hasLB = text.indexOf(EOL) > 0;
            if (hasLB) {
                text = text.split(EOL).map(function (m) {
                    return m.replace(/^\s+|\s+$/g, '');
                }).join('\\n');
            }
            var hasTabs = text.indexOf('\t') > 0;
            if (hasLB || hasTabs) {
                var prev = idx ? sql[idx - 1] : '';
                if (prev !== 'E' && prev !== 'e') {
                    var r = result ? result[result.length - 1] : '';
                    if (r && r !== ' ' && compressors.indexOf(r) < 0) {
                        result += ' ';
                    }
                    result += 'E';
                }
                if (hasTabs) {
                    text = text.replace(/\t/g, '\\t');
                }
            }
            result += text;
            idx = closeIdx;
            skipGaps();
            continue;
        }

        if (compress && compressors.indexOf(s) >= 0) {
            space = false;
            skipGaps();
        }

        addSpace();
        result += s;

    } while (++idx < len);

    return result;

    function skipGaps() {
        if (compress) {
            while (idx < len - 1 && isGap(sql[id ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.minify.SQLParsingError"></a>[function <span class="apidocSignatureSpan">pg-promise.</span>minify.SQLParsingError (code, position)](#apidoc.element.pg-promise.minify.SQLParsingError)
- description and source-code
```javascript
function SQLParsingError(code, position) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'SQLParsingError';
    this.stack = temp.stack;
    this.code = code; // one of parsingErrorCode values;
    this.error = errorMessages[code].message;
    this.position = position; // Error position in the text: {line, column}
    this.message = "Error parsing SQL at {line:" + position.line + ",col:" + position.column + "}: " + this.error;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg-promise.ParameterizedQuery"></a>[module pg-promise.ParameterizedQuery](#apidoc.module.pg-promise.ParameterizedQuery)

#### <a name="apidoc.element.pg-promise.ParameterizedQuery.ParameterizedQuery"></a>[function <span class="apidocSignatureSpan">pg-promise.</span>ParameterizedQuery (text, values)](#apidoc.element.pg-promise.ParameterizedQuery.ParameterizedQuery)
- description and source-code
```javascript
function ParameterizedQuery(text, values) {
    if (!(this instanceof ParameterizedQuery)) {
        return new ParameterizedQuery(text, values);
    }

    var currentError, PQ = {}, changed = true, state = {
        text: text,
        binary: undefined,
        rowMode: undefined
    };

    function setValues(v) {
        if (Array.isArray(v)) {
            if (v.length) {
                PQ.values = v;
            } else {
                delete PQ.values;
            }
        } else {
            if ($npm.utils.isNull(v)) {
                delete PQ.values;
            } else {
                PQ.values = [v];
            }
        }
    }

    setValues(values);

    /**
     * @name ParameterizedQuery#text
     * @type {string|QueryFile}
     * @description
     * A non-empty query string or a {@link QueryFile} object.
     */
    Object.defineProperty(this, 'text', {
        get: () => state.text,
        set: value => {
            if (value !== state.text) {
                state.text = value;
                changed = true;
            }
        }
    });

    /**
     * @name ParameterizedQuery#values
     * @type {array}
     * @description
     * Query formatting parameters, depending on the type:
     *
     * - 'null' / 'undefined' means the query has no formatting parameters
     * - 'Array' - it is an array of formatting parameters
     * - None of the above, means it is a single formatting value, which
     *   is then automatically wrapped into an array
     */
    Object.defineProperty(this, 'values', {
        get: () => PQ.values,
        set: value => {
            setValues(value);
        }
    });

    /**
     * @name ParameterizedQuery#binary
     * @type {boolean}
     * @default undefined
     * @description
     * Activates binary result mode. The default is the text mode.
     *
     * @see {@link http://www.postgresql.org/docs/devel/static/protocol-flow.html#PROTOCOL-FLOW-EXT-QUERY Extended Query}
     */
    Object.defineProperty(this, 'binary', {
        get: () => state.binary,
        set: value => {
            if (value !== state.binary) {
                state.binary = value;
                changed = true;
            }
        }
    });

    /**
     * @name ParameterizedQuery#rowMode
     * @type {string}
     * @default undefined
     * @description
     * Changes the way data arrives to the client, with only one value supported by $[pg]:
     *  - 'rowMode = 'array'' will make all data rows arrive as arrays of values.
     *    By default, rows arrive as objects.
     */
    Object.defineProperty(this, 'rowMode', {
        get: () => state.rowMode,
        set: value => {
            if (value !== state.rowMode) {
                state.rowMode = value;
                changed = true;
            }
        }
    });

    /**
     * @name ParameterizedQuery#error
     * @type {errors.ParameterizedQueryError}
     * @default undefined
     * @readonly
     * @description
     * When in an error state, it is set to a {@link errors.ParameterizedQueryError ParameterizedQueryError} object. Otherwise,
it is 'undefined'.
     *
     * This property is primarily for internal use by the library.
     */
    Object.defineProperty(this, 'error', {
        get: () => currentError
    });

    if ($npm.utils.isObject(text, ['text'])) {
        state.text = text.text;
        state.binary = text.binary;
        state.rowMode = text.rowMode;
        setValues(text.values);
    }

    /**
     * @method ParameterizedQuery.parse
     * @description
     * Parses the current object and returns a simple '{text, values}', if successful,
     * or else it returns a {@link errors.ParameterizedQueryError ParameterizedQueryError} object.
     *
     * This method is primarily for internal use by the library.
     *
     * @returns {{text, values}|errors.ParameterizedQueryError}
     */
    this.parse = () => {

        var qf = state.text instanceof $npm.QueryFile ? s ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg-promise.ParameterizedQuery.prototype"></a>[module pg-promise.ParameterizedQuery.prototype](#apidoc.module.pg-promise.ParameterizedQuery.prototype)

#### <a name="apidoc.element.pg-promise.ParameterizedQuery.prototype.toString"></a>[function <span class="apidocSignatureSpan">pg-promise.ParameterizedQuery.prototype.</span>toString (level)](#apidoc.element.pg-promise.ParameterizedQuery.prototype.toString)
- description and source-code
```javascript
toString = function (level) {
    level = level > 0 ? parseInt(level) : 0;
    var gap = $npm.utils.messageGap(level + 1);
    var pq = this.parse();
    var lines = [
        'ParameterizedQuery {'
    ];
    if ($npm.utils.isText(pq.text)) {
        lines.push(gap + 'text: "' + pq.text + '"');
    }
    if (this.values !== undefined) {
        lines.push(gap + 'values: ' + JSON.stringify(this.values));
    }
    if (this.binary !== undefined) {
        lines.push(gap + 'binary: ' + JSON.stringify(this.binary));
    }
    if (this.rowMode !== undefined) {
        lines.push(gap + 'rowMode: ' + JSON.stringify(this.rowMode));
    }
    if (this.error !== undefined) {
        lines.push(gap + 'error: ' + this.error.toString(level + 1));
    }
    lines.push($npm.utils.messageGap(level) + '}');
    return lines.join($npm.os.EOL);
}
```
- example usage
```shell
...
 *
 * @param {boolean} [raw=false]
 * Indicates when not to escape the resulting text.
 *
 * @returns {string}
 *
 * - 'null' string, if the 'value' resolves as 'null' or 'undefined'
 * - escaped result of 'value.toString()', if the 'value' isn't a string
 * - escaped string version, if 'value' is a string.
 *
 *  The result is not escaped, if 'raw' was passed in as 'true'.
 */
text: (value, raw) => {
    value = resolveFunc(value);
    if (isNull(value)) {
...
```



# <a name="apidoc.module.pg-promise.PreparedStatement"></a>[module pg-promise.PreparedStatement](#apidoc.module.pg-promise.PreparedStatement)

#### <a name="apidoc.element.pg-promise.PreparedStatement.PreparedStatement"></a>[function <span class="apidocSignatureSpan">pg-promise.</span>PreparedStatement (name, text, values)](#apidoc.element.pg-promise.PreparedStatement.PreparedStatement)
- description and source-code
```javascript
function PreparedStatement(name, text, values) {
    if (!(this instanceof PreparedStatement)) {
        return new PreparedStatement(name, text, values);
    }

    var currentError, PS = {}, changed = true, state = {
        name: name,
        text: text,
        binary: undefined,
        rowMode: undefined,
        rows: undefined
    };

    function setValues(v) {
        if (Array.isArray(v)) {
            if (v.length) {
                PS.values = v;
            } else {
                delete PS.values;
            }
        } else {
            if ($npm.utils.isNull(v)) {
                delete PS.values;
            } else {
                PS.values = [v];
            }
        }
    }

    setValues(values);

    /**
     * @name PreparedStatement#name
     * @type {string}
     * @description
     * An arbitrary name given to this particular prepared statement. It must be unique within a single session and is
     * subsequently used to execute or deallocate a previously prepared statement.
     */
    Object.defineProperty(this, 'name', {
        get: () => state.name,
        set: value => {
            if (value !== state.name) {
                state.name = value;
                changed = true;
            }
        }
    });

    /**
     * @name PreparedStatement#text
     * @type {string|QueryFile}
     * @description
     * A non-empty query string or a {@link QueryFile} object.
     *
     * Changing this property for the same {@link PreparedStatement#name name} will have no effect, because queries
     * for Prepared Statements are cached, with {@link PreparedStatement#name name} being the cache key.
     */
    Object.defineProperty(this, 'text', {
        get: () => state.text,
        set: value => {
            if (value !== state.text) {
                state.text = value;
                changed = true;
            }
        }
    });

    /**
     * @name PreparedStatement#values
     * @type {array}
     * @description
     * Query formatting parameters, depending on the type:
     *
     * - 'null' / 'undefined' means the query has no formatting parameters
     * - 'Array' - it is an array of formatting parameters
     * - None of the above, means it is a single formatting value, which
     *   is then automatically wrapped into an array
     */
    Object.defineProperty(this, 'values', {
        get: () => PS.values,
        set: value => {
            setValues(value);
        }
    });

    /**
     * @name PreparedStatement#binary
     * @type {boolean}
     * @default undefined
     * @description
     * Activates binary result mode. The default is the text mode.
     *
     * @see {@link http://www.postgresql.org/docs/devel/static/protocol-flow.html#PROTOCOL-FLOW-EXT-QUERY Extended Query}
     */
    Object.defineProperty(this, 'binary', {
        get: () => state.binary,
        set: value => {
            if (value !== state.binary) {
                state.binary = value;
                changed = true;
            }
        }
    });

    /**
     * @name PreparedStatement#rowMode
     * @type {string}
     * @default undefined
     * @description
     * Changes the way data arrives to the client, with only one value supported by $[pg]:
     *  - 'rowMode = 'array'' will make all data rows arrive as arrays of values.
     *    By default, rows arrive as objects.
     */
    Object.defineProperty(this, 'rowMode', {
        get: () => state.rowMode,
        set: value => {
            if (value !== state.rowMode) {
                state.rowMode = value;
                changed = true;
            }
        }
    });

    /**
     * @name PreparedStatement#rows
     * @type {number}
     * @description
     * Number of rows to return at a time from a Prepared Statement's portal.
     * The default is 0, which means that all rows must be returned at once.
     */
    Object.defineProperty(this, 'rows', {
        get: () => state.rows,
        set: val ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg-promise.PreparedStatement.prototype"></a>[module pg-promise.PreparedStatement.prototype](#apidoc.module.pg-promise.PreparedStatement.prototype)

#### <a name="apidoc.element.pg-promise.PreparedStatement.prototype.toString"></a>[function <span class="apidocSignatureSpan">pg-promise.PreparedStatement.prototype.</span>toString (level)](#apidoc.element.pg-promise.PreparedStatement.prototype.toString)
- description and source-code
```javascript
toString = function (level) {
    level = level > 0 ? parseInt(level) : 0;
    var gap = $npm.utils.messageGap(level + 1);
    var ps = this.parse();
    var lines = [
        'PreparedStatement {',
        gap + 'name: ' + JSON.stringify(this.name)
    ];
    if ($npm.utils.isText(ps.text)) {
        lines.push(gap + 'text: "' + ps.text + '"');
    }
    if (this.values !== undefined) {
        lines.push(gap + 'values: ' + JSON.stringify(this.values));
    }
    if (this.binary !== undefined) {
        lines.push(gap + 'binary: ' + JSON.stringify(this.binary));
    }
    if (this.rowMode !== undefined) {
        lines.push(gap + 'rowMode: ' + JSON.stringify(this.rowMode));
    }
    if (this.rows !== undefined) {
        lines.push(gap + 'rows: ' + JSON.stringify(this.rows));
    }
    if (this.error) {
        lines.push(gap + 'error: ' + this.error.toString(level + 1));
    }
    lines.push($npm.utils.messageGap(level) + '}');
    return lines.join($npm.os.EOL);
}
```
- example usage
```shell
...
 *
 * @param {boolean} [raw=false]
 * Indicates when not to escape the resulting text.
 *
 * @returns {string}
 *
 * - 'null' string, if the 'value' resolves as 'null' or 'undefined'
 * - escaped result of 'value.toString()', if the 'value' isn't a string
 * - escaped string version, if 'value' is a string.
 *
 *  The result is not escaped, if 'raw' was passed in as 'true'.
 */
text: (value, raw) => {
    value = resolveFunc(value);
    if (isNull(value)) {
...
```



# <a name="apidoc.module.pg-promise.QueryFile"></a>[module pg-promise.QueryFile](#apidoc.module.pg-promise.QueryFile)

#### <a name="apidoc.element.pg-promise.QueryFile.QueryFile"></a>[function <span class="apidocSignatureSpan">pg-promise.</span>QueryFile (file, options)](#apidoc.element.pg-promise.QueryFile.QueryFile)
- description and source-code
```javascript
function QueryFile(file, options) {

    if (!(this instanceof QueryFile)) {
        return new QueryFile(file, options);
    }

    var sql, error, ready, modTime, after, filePath = file, opt = {
        debug: $npm.utils.isDev(),
        minify: false,
        compress: false
    };

    if (options && typeof options === 'object') {
        if (options.debug !== undefined) {
            opt.debug = !!options.debug;
        }
        if (options.minify !== undefined) {
            after = options.minify === 'after';
            opt.minify = after ? 'after' : !!options.minify;
        }
        if (options.compress !== undefined) {
            opt.compress = !!options.compress;
        }
        if (opt.compress && options.minify === undefined) {
            opt.minify = true;
        }
        if (options.params !== undefined) {
            opt.params = options.params;
        }
    }

    Object.freeze(opt);

    if ($npm.utils.isText(filePath) && !$npm.utils.isPathAbsolute(filePath)) {
        filePath = $npm.path.join($npm.utils.startDir, filePath);
    }

    // Custom Type Formatting support:
    this.formatDBType = function () {
        this.prepare(true);
        return this.query;
    };

    /**
     * @method QueryFile.prepare
     * @summary Prepares the query for execution.
     * @description
     * If the the query hasn't been prepared yet, it will read the file and process the contents according
     * to the parameters passed into the constructor.
     *
     * This method is primarily for internal use by the library.
     *
     * @param {boolean} [throwErrors=false]
     * Throw any error encountered.
     *
     */
    this.prepare = function (throwErrors) {
        var lastMod;
        if (opt.debug && ready) {
            try {
                lastMod = $npm.fs.statSync(filePath).mtime.getTime();
                if (lastMod === modTime) {
                    // istanbul ignore next;
                    // coverage for this works differently under Windows and Linux
                    return;
                }
                ready = false;
            } catch (e) {
                sql = undefined;
                ready = false;
                error = e;
                if (throwErrors) {
                    throw error;
                }
                return;
            }
        }
        if (ready) {
            return;
        }
        try {
            sql = $npm.fs.readFileSync(filePath, 'utf8');
            modTime = lastMod || $npm.fs.statSync(filePath).mtime.getTime();
            if (opt.minify && !after) {
                sql = $npm.minify(sql, {compress: opt.compress});
            }
            if (opt.params !== undefined) {
                sql = $npm.format(sql, opt.params, {partial: true});
            }
            if (opt.minify && after) {
                sql = $npm.minify(sql, {compress: opt.compress});
            }
            ready = true;
            error = undefined;
        } catch (e) {
            sql = undefined;
            error = new $npm.QueryFileError(e, this);
            if (throwErrors) {
                throw error;
            }
        }
    };

    /**
     * @name QueryFile#query
     * @type {string}
     * @default undefined
     * @readonly
     * @summary Prepared query string.
     * @description
     * When property {@link QueryFile#error error} is set, the query is 'undefined'.
     *
     * This property is primarily for internal use by the library.
     */
    Object.defineProperty(this, 'query', {
        get: () => sql
    });

    /**
     * @name QueryFile#error
     * @type {errors.QueryFileError}
     * @default undefined
     * @readonly
     * @description
     * When in an error state, it is set to a {@link errors.QueryFileError QueryFileError} object. Otherwise, it is 'undefined'.
     *
     * This property is primarily for internal use by the library.
     */
    Object.defineProperty(this, 'error', { ...
```
- example usage
```shell
...

Example:

'''js
// Helper for linking to external query files:
function sql(file) {
// consider using here: path.join(__dirname, file)
return new pgp.QueryFile(file, {minify: true});
}

// Create QueryFile globally, once per file:
var sqlFindUser = sql('./sql/findUser.sql');

db.one(sqlFindUser, {id: 123})
.then(user=> {
...
```



# <a name="apidoc.module.pg-promise.QueryFile.prototype"></a>[module pg-promise.QueryFile.prototype](#apidoc.module.pg-promise.QueryFile.prototype)

#### <a name="apidoc.element.pg-promise.QueryFile.prototype.inspect"></a>[function <span class="apidocSignatureSpan">pg-promise.QueryFile.prototype.</span>inspect ()](#apidoc.element.pg-promise.QueryFile.prototype.inspect)
- description and source-code
```javascript
inspect = function () {
    return this.toString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.QueryFile.prototype.toString"></a>[function <span class="apidocSignatureSpan">pg-promise.QueryFile.prototype.</span>toString (level)](#apidoc.element.pg-promise.QueryFile.prototype.toString)
- description and source-code
```javascript
toString = function (level) {
    level = level > 0 ? parseInt(level) : 0;
    var gap = $npm.utils.messageGap(level + 1);
    var lines = [
        'QueryFile {'
    ];
    this.prepare();
    lines.push(gap + 'file: "' + this.file + '"');
    lines.push(gap + 'options: ' + JSON.stringify(this.options));
    if (this.error) {
        lines.push(gap + 'error: ' + this.error.toString(level + 1));
    } else {
        lines.push(gap + 'query: "' + this.query + '"');
    }
    lines.push($npm.utils.messageGap(level) + '}');
    return lines.join($npm.os.EOL);
}
```
- example usage
```shell
...
 *
 * @param {boolean} [raw=false]
 * Indicates when not to escape the resulting text.
 *
 * @returns {string}
 *
 * - 'null' string, if the 'value' resolves as 'null' or 'undefined'
 * - escaped result of 'value.toString()', if the 'value' isn't a string
 * - escaped string version, if 'value' is a string.
 *
 *  The result is not escaped, if 'raw' was passed in as 'true'.
 */
text: (value, raw) => {
    value = resolveFunc(value);
    if (isNull(value)) {
...
```



# <a name="apidoc.module.pg-promise.array"></a>[module pg-promise.array](#apidoc.module.pg-promise.array)

#### <a name="apidoc.element.pg-promise.array.countIf"></a>[function <span class="apidocSignatureSpan">pg-promise.array.</span>countIf (arr, cb, obj)](#apidoc.element.pg-promise.array.countIf)
- description and source-code
```javascript
function countIf(arr, cb, obj) {
    var count = 0;
    if (obj) {
        for (var i = 0; i < arr.length; i++) {
            count += cb.call(obj, arr[i], i, arr) ? 1 : 0;
        }
    } else {
        for (var k = 0; k < arr.length; k++) {
            count += cb(arr[k], k, arr) ? 1 : 0;
        }
    }
    return count;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.array.filter"></a>[function <span class="apidocSignatureSpan">pg-promise.array.</span>filter (arr, cb, obj)](#apidoc.element.pg-promise.array.filter)
- description and source-code
```javascript
function filter(arr, cb, obj) {
    var res = [];
    if (obj) {
        for (var i = 0; i < arr.length; i++) {
            if (cb.call(obj, arr[i], i, arr)) {
                res.push(arr[i]);
            }
        }
    } else {
        for (var k = 0; k < arr.length; k++) {
            if (cb(arr[k], k, arr)) {
                res.push(arr[k]);
            }
        }
    }
    return res;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.array.forEach"></a>[function <span class="apidocSignatureSpan">pg-promise.array.</span>forEach (arr, cb, obj)](#apidoc.element.pg-promise.array.forEach)
- description and source-code
```javascript
function forEach(arr, cb, obj) {
    if (obj) {
        for (var i = 0; i < arr.length; i++) {
            cb.call(obj, arr[i], i, arr);
        }
    } else {
        for (var k = 0; k < arr.length; k++) {
            cb(arr[k], k, arr);
        }
    }
}
```
- example usage
```shell
...
* Executes a provided function once per array element, for an array of rows resolved by method {@link Database.any any}.
*
* It is a convenience method to reduce the following code:
*
* '''js
* db.any(query, values)
*     .then(data => {
*         data.forEach((row, index, data) => {
*              // process the row
*         });
*         return data;
*     });
* '''
*
* In addition to much shorter code, it offers the following benefits:
...
```

#### <a name="apidoc.element.pg-promise.array.map"></a>[function <span class="apidocSignatureSpan">pg-promise.array.</span>map (arr, cb, obj)](#apidoc.element.pg-promise.array.map)
- description and source-code
```javascript
function map(arr, cb, obj) {
    var res = new Array(arr.length);
    if (obj) {
        for (var i = 0; i < arr.length; i++) {
            res[i] = cb.call(obj, arr[i], i, arr);
        }
    } else {
        for (var k = 0; k < arr.length; k++) {
            res[k] = cb(arr[k], k, arr);
        }
    }
    return res;
}
```
- example usage
```shell
...
'''js
query('INSERT INTO $1~($2~) VALUES(...)', ['Table Name', 'Column Name']);
//=> INSERT INTO "Table Name"("Column Name") VALUES(...)

// A mixed example for a dynamic column list:
var columns = ['id', 'message'];
query('SELECT ${columns^} FROM ${table~}', {
    columns: columns.map(pgp.as.name).join(),
    table: 'Table Name'
});
//=> SELECT "id","message" FROM "Table Name"
'''

Version 5.2.1 and later supports extended syntax for '${this~}' and for method [as.name]:
...
```



# <a name="apidoc.module.pg-promise.as"></a>[module pg-promise.as](#apidoc.module.pg-promise.as)

#### <a name="apidoc.element.pg-promise.as.array"></a>[function <span class="apidocSignatureSpan">pg-promise.as.</span>array (arr)](#apidoc.element.pg-promise.as.array)
- description and source-code
```javascript
arr => {
    arr = resolveFunc(arr);
    if (isNull(arr)) {
        return 'null';
    }
    if (arr instanceof Array) {
        return formatArray(arr);
    }
    throw new TypeError(wrapText(arr) + ' is not an Array object.');
}
```
- example usage
```shell
...
   - format '$1' (single variable), if 'values' is of type 'string', 'boolean', 'number', 'Date', 'function', 'null' or [QueryFile
];
   - format '$1, $2, etc..', if 'values' is an array;
   - format '$*propName*', if 'values' is an object (not 'null' and not 'Date'), where '*' is any of the supported open-close pairs
: '{}', '()', '<>', '[]', '//';
* 'values' (optional) - value/array/object to replace the variables in the query;
* 'qrm' - (optional) *Query Result Mask*, as explained below. When not passed, it defaults to 'pgp.queryResult.any'.

When a value/property inside array/object is an array, it is treated as a [PostgreSQL Array Type](http://www.postgresql.org/docs
/9.4/static/arrays.html),
converted into the array constructor format of 'array[]', the same as calling method 'pgp.as.array()'.

When a value/property inside array/object is of type 'object' (except for 'null', 'Date' or 'Buffer'), it is automatically
serialized into JSON, the same as calling method 'pgp.as.json()', except the latter would convert anything to JSON.

For the latest SQL formatting support see the API: methods [query] and [as.format].

### SQL Names
...
```

#### <a name="apidoc.element.pg-promise.as.bool"></a>[function <span class="apidocSignatureSpan">pg-promise.as.</span>bool (value)](#apidoc.element.pg-promise.as.bool)
- description and source-code
```javascript
value => {
    value = resolveFunc(value);
    if (isNull(value)) {
        return 'null';
    }
    return value ? 'true' : 'false';
}
```
- example usage
```shell
...
    return 'null';
}

switch (typeof value) {
    case 'string':
        return $as.text(value, isRaw);
    case 'boolean':
        return $as.bool(value);
    case 'number':
        return $as.number(value);
    default:
        if (value instanceof Date) {
            return $as.date(value, isRaw);
        }
        if (value instanceof Array) {
...
```

#### <a name="apidoc.element.pg-promise.as.buffer"></a>[function <span class="apidocSignatureSpan">pg-promise.as.</span>buffer (obj, raw)](#apidoc.element.pg-promise.as.buffer)
- description and source-code
```javascript
(obj, raw) => {
    obj = resolveFunc(obj);
    if (isNull(obj)) {
        throwIfRaw(raw);
        return 'null';
    }
    if (obj instanceof Buffer) {
        var s = '\\x' + obj.toString('hex');
        return raw ? s : wrapText(s);
    }
    throw new TypeError(wrapText(obj) + ' is not a Buffer object.');
}
```
- example usage
```shell
...
            if (value instanceof Date) {
                return $as.date(value, isRaw);
            }
            if (value instanceof Array) {
                return $as.array(value);
            }
            if (value instanceof Buffer) {
                return $as.buffer(value, isRaw);
            }
            return $as.json(value, isRaw);
    }
}

//////////////////////////////////////////////////////////////////////////
// Converts array of values into PostgreSQL Array Constructor: array[...],
...
```

#### <a name="apidoc.element.pg-promise.as.csv"></a>[function <span class="apidocSignatureSpan">pg-promise.as.</span>csv (resolveFunc(values)](#apidoc.element.pg-promise.as.csv)
- description and source-code
```javascript
values => formatCSV(resolveFunc(values))
```
- example usage
```shell
...

switch (fm) {
    case fmFlags.name:
        return $as.name(value);
    case fmFlags.json:
        return $as.json(value, isRaw);
    case fmFlags.csv:
        return $as.csv(value);
    case fmFlags.value:
        return $as.value(value);
    default:
        break;
}

if (isNull(value)) {
...
```

#### <a name="apidoc.element.pg-promise.as.date"></a>[function <span class="apidocSignatureSpan">pg-promise.as.</span>date (d, raw)](#apidoc.element.pg-promise.as.date)
- description and source-code
```javascript
(d, raw) => {
    d = resolveFunc(d);
    if (isNull(d)) {
        throwIfRaw(raw);
        return 'null';
    }
    if (d instanceof Date) {
        var s = $pgUtils.prepareValue(d);
        return raw ? s : wrapText(s);
    }
    throw new TypeError(wrapText(d) + ' is not a Date object.');
}
```
- example usage
```shell
...
    return $as.text(value, isRaw);
case 'boolean':
    return $as.bool(value);
case 'number':
    return $as.number(value);
default:
    if (value instanceof Date) {
        return $as.date(value, isRaw);
    }
    if (value instanceof Array) {
        return $as.array(value);
    }
    if (value instanceof Buffer) {
        return $as.buffer(value, isRaw);
    }
...
```

#### <a name="apidoc.element.pg-promise.as.format"></a>[function <span class="apidocSignatureSpan">pg-promise.as.</span>format (query, values, options)](#apidoc.element.pg-promise.as.format)
- description and source-code
```javascript
(query, values, options) => {
    if (query && typeof query.formatDBType === 'function') {
        query = query.formatDBType();
    }
    return $formatQuery(query, values, false, options);
}
```
- example usage
```shell
...
* @param {external:Stream} stream
* Stream object to initialize streaming.
*
* @example
* var QueryStream = require('pg-query-stream');
* var JSONStream = require('JSONStream');
*
* // you can also use pgp.as.format(query, values, options)
* // to format queries properly, via pg-promise;
* var qs = new QueryStream('select * from users');
*
* db.stream(qs, stream => {
*         // initiate streaming into the console:
*         stream.pipe(JSONStream.stringify()).pipe(process.stdout);
*     })
...
```

#### <a name="apidoc.element.pg-promise.as.func"></a>[function <span class="apidocSignatureSpan">pg-promise.as.</span>func (func, raw, obj)](#apidoc.element.pg-promise.as.func)
- description and source-code
```javascript
(func, raw, obj) => {
    if (isNull(func)) {
        throwIfRaw(raw);
        return 'null';
    }
    if (typeof func !== 'function') {
        throw new TypeError(wrapText(func) + ' is not a function.');
    }
    var fm = raw ? fmFlags.raw : null;
    if (isNull(obj)) {
        return formatValue(resolveFunc(func), fm);
    }
    if (typeof obj === 'object') {
        return formatValue(resolveFunc(func, obj), fm, obj);
    }
    throw new TypeError(wrapText(obj) + ' is not an object.');
}
```
- example usage
```shell
...

In PostgreSQL stored procedures are just functions that usually do not return anything.

Suppose we want to call function **findAudit** to find audit records by 'user_id' and maximum timestamp.
We can make such call as shown below:

'''js
db.func('findAudit', [123, new Date()])
    .then(data => {
        console.log(data); // printing the data returned
    })
    .catch(error => {
        console.log(error); // printing the error
    });
'''
...
```

#### <a name="apidoc.element.pg-promise.as.json"></a>[function <span class="apidocSignatureSpan">pg-promise.as.</span>json (obj, raw)](#apidoc.element.pg-promise.as.json)
- description and source-code
```javascript
(obj, raw) => {
    obj = resolveFunc(obj);
    if (isNull(obj)) {
        throwIfRaw(raw);
        return 'null';
    }
    var s = JSON.stringify(obj);
    return raw ? s : wrapText(safeText(s));
}
```
- example usage
```shell
...
* 'values' (optional) - value/array/object to replace the variables in the query;
* 'qrm' - (optional) *Query Result Mask*, as explained below. When not passed, it defaults to 'pgp.queryResult.any'.

When a value/property inside array/object is an array, it is treated as a [PostgreSQL Array Type](http://www.postgresql.org/docs
/9.4/static/arrays.html),
converted into the array constructor format of 'array[]', the same as calling method 'pgp.as.array()'.

When a value/property inside array/object is of type 'object' (except for 'null', 'Date' or 'Buffer'), it is automatically
serialized into JSON, the same as calling method 'pgp.as.json()', except the latter would convert anything to JSON.

For the latest SQL formatting support see the API: methods [query] and [as.format].

### SQL Names

When a variable ends with '~' (tilde) or ':name', it represents an SQL name or identifier, which must be a text
string of at least 1 character long. Such name is then properly escaped and wrapped in double quotes.
...
```

#### <a name="apidoc.element.pg-promise.as.name"></a>[function <span class="apidocSignatureSpan">pg-promise.as.</span>name (name)](#apidoc.element.pg-promise.as.name)
- description and source-code
```javascript
name => {
    name = resolveFunc(name);
    if (name) {
        if (typeof name === 'string') {
            return /^\s*\*(\s*)$/.test(name) ? name : formatName(name);
        }
        if (typeof name === 'object') {
            var keys = Array.isArray(name) ? name : Object.keys(name);
            if (!keys.length) {
                throw new Error('Cannot retrieve sql names from an empty array/object.');
            }
            return $arr.map(keys, value => {
                if (!value || typeof value !== 'string') {
                    throw new Error('Invalid sql name: ' + JSON.stringify(value));
                }
                return formatName(value);
            }).join();
        }
    }

    throw new TypeError('Invalid sql name: ' + JSON.stringify(name));

    function formatName(name) {
        return '"' + name.replace(/"/g, '""') + '"';
    }
}
```
- example usage
```shell
...
}

var isRaw = !!(fm & fmFlags.raw);
fm &= ~fmFlags.raw;

switch (fm) {
    case fmFlags.name:
        return $as.name(value);
    case fmFlags.json:
        return $as.json(value, isRaw);
    case fmFlags.csv:
        return $as.csv(value);
    case fmFlags.value:
        return $as.value(value);
    default:
...
```

#### <a name="apidoc.element.pg-promise.as.number"></a>[function <span class="apidocSignatureSpan">pg-promise.as.</span>number (num)](#apidoc.element.pg-promise.as.number)
- description and source-code
```javascript
num => {
    num = resolveFunc(num);
    if (isNull(num)) {
        return 'null';
    }
    if (typeof num !== 'number') {
        throw new TypeError(wrapText(num) + ' is not a number.');
    }
    if (isFinite(num)) {
        return num.toString();
    }
    // Converting NaN/+Infinity/-Infinity according to Postgres documentation:
    // http://www.postgresql.org/docs/9.4/static/datatype-numeric.html#DATATYPE-FLOAT
    //
    // NOTE: strings for 'NaN'/'+Infinity'/'-Infinity' are not case-sensitive.
    if (num === Number.POSITIVE_INFINITY) {
        return wrapText('+Infinity');
    }
    if (num === Number.NEGATIVE_INFINITY) {
        return wrapText('-Infinity');
    }
    return wrapText('NaN');
}
```
- example usage
```shell
...

    switch (typeof value) {
case 'string':
    return $as.text(value, isRaw);
case 'boolean':
    return $as.bool(value);
case 'number':
    return $as.number(value);
default:
    if (value instanceof Date) {
        return $as.date(value, isRaw);
    }
    if (value instanceof Array) {
        return $as.array(value);
    }
...
```

#### <a name="apidoc.element.pg-promise.as.text"></a>[function <span class="apidocSignatureSpan">pg-promise.as.</span>text (value, raw)](#apidoc.element.pg-promise.as.text)
- description and source-code
```javascript
(value, raw) => {
    value = resolveFunc(value);
    if (isNull(value)) {
        throwIfRaw(raw);
        return 'null';
    }
    if (typeof value !== 'string') {
        value = value.toString();
    }
    return raw ? value : wrapText(safeText(value));
}
```
- example usage
```shell
...
if (isNull(value)) {
    throwIfRaw(isRaw);
    return 'null';
}

switch (typeof value) {
    case 'string':
        return $as.text(value, isRaw);
    case 'boolean':
        return $as.bool(value);
    case 'number':
        return $as.number(value);
    default:
        if (value instanceof Date) {
            return $as.date(value, isRaw);
...
```

#### <a name="apidoc.element.pg-promise.as.value"></a>[function <span class="apidocSignatureSpan">pg-promise.as.</span>value (value)](#apidoc.element.pg-promise.as.value)
- description and source-code
```javascript
value => {
    value = resolveFunc(value);
    if (isNull(value)) {
        throw new TypeError('Open values cannot be null or undefined.');
    }
    return safeText(formatValue(value, fmFlags.raw));
}
```
- example usage
```shell
...
    case fmFlags.name:
        return $as.name(value);
    case fmFlags.json:
        return $as.json(value, isRaw);
    case fmFlags.csv:
        return $as.csv(value);
    case fmFlags.value:
        return $as.value(value);
    default:
        break;
}

if (isNull(value)) {
    throwIfRaw(isRaw);
    return 'null';
...
```



# <a name="apidoc.module.pg-promise.errors"></a>[module pg-promise.errors](#apidoc.module.pg-promise.errors)

#### <a name="apidoc.element.pg-promise.errors.ParameterizedQueryError"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.</span>ParameterizedQueryError (error, ps)](#apidoc.element.pg-promise.errors.ParameterizedQueryError)
- description and source-code
```javascript
function ParameterizedQueryError(error, ps) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'ParameterizedQueryError';
    this.stack = temp.stack;
    if (error instanceof $npm.QueryFileError) {
        this.error = error;
        this.message = 'Failed to initialize \'text\' from a QueryFile.';
    } else {
        this.message = error;
    }
    this.result = ps;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.errors.PreparedStatementError"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.</span>PreparedStatementError (error, ps)](#apidoc.element.pg-promise.errors.PreparedStatementError)
- description and source-code
```javascript
function PreparedStatementError(error, ps) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'PreparedStatementError';
    this.stack = temp.stack;
    if (error instanceof $npm.QueryFileError) {
        this.error = error;
        this.message = 'Failed to initialize \'text\' from a QueryFile.';
    } else {
        this.message = error;
    }
    this.result = ps;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.errors.QueryFileError"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.</span>QueryFileError (error, qf)](#apidoc.element.pg-promise.errors.QueryFileError)
- description and source-code
```javascript
function QueryFileError(error, qf) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'QueryFileError';
    this.stack = temp.stack;
    if (error instanceof $npm.minify.SQLParsingError) {
        this.error = error;
        this.message = 'Failed to parse the SQL.';
    } else {
        this.message = error.message;
    }
    this.file = qf.file;
    this.options = qf.options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.errors.QueryResultError"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.</span>QueryResultError (code, result, query, values)](#apidoc.element.pg-promise.errors.QueryResultError)
- description and source-code
```javascript
function QueryResultError(code, result, query, values) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'QueryResultError';
    this.stack = temp.stack;
    this.message = errorMessages[code].message;
    this.code = code;
    this.result = result;
    this.query = query;
    this.values = values;
    this.received = result.rows.length;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg-promise.errors.ParameterizedQueryError"></a>[module pg-promise.errors.ParameterizedQueryError](#apidoc.module.pg-promise.errors.ParameterizedQueryError)

#### <a name="apidoc.element.pg-promise.errors.ParameterizedQueryError.ParameterizedQueryError"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.</span>ParameterizedQueryError (error, ps)](#apidoc.element.pg-promise.errors.ParameterizedQueryError.ParameterizedQueryError)
- description and source-code
```javascript
function ParameterizedQueryError(error, ps) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'ParameterizedQueryError';
    this.stack = temp.stack;
    if (error instanceof $npm.QueryFileError) {
        this.error = error;
        this.message = 'Failed to initialize \'text\' from a QueryFile.';
    } else {
        this.message = error;
    }
    this.result = ps;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg-promise.errors.ParameterizedQueryError.prototype"></a>[module pg-promise.errors.ParameterizedQueryError.prototype](#apidoc.module.pg-promise.errors.ParameterizedQueryError.prototype)

#### <a name="apidoc.element.pg-promise.errors.ParameterizedQueryError.prototype.inspect"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.ParameterizedQueryError.prototype.</span>inspect ()](#apidoc.element.pg-promise.errors.ParameterizedQueryError.prototype.inspect)
- description and source-code
```javascript
inspect = function () {
    return this.toString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.errors.ParameterizedQueryError.prototype.toString"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.ParameterizedQueryError.prototype.</span>toString (level)](#apidoc.element.pg-promise.errors.ParameterizedQueryError.prototype.toString)
- description and source-code
```javascript
toString = function (level) {
    level = level > 0 ? parseInt(level) : 0;
    var gap0 = $npm.utils.messageGap(level),
        gap1 = $npm.utils.messageGap(level + 1),
        gap2 = $npm.utils.messageGap(level + 2),
        lines = [
            'ParameterizedQueryError {',
            gap1 + 'message: "' + this.message + '"',
            gap1 + 'result: {',
            gap2 + 'text: ' + JSON.stringify(this.result.text),
            gap2 + 'values: ' + JSON.stringify(this.result.values),
            gap1 + '}'
        ];
    if (this.error) {
        lines.push(gap1 + 'error: ' + this.error.toString(level + 1));
    }
    lines.push(gap0 + '}');
    return lines.join($npm.os.EOL);
}
```
- example usage
```shell
...
 *
 * @param {boolean} [raw=false]
 * Indicates when not to escape the resulting text.
 *
 * @returns {string}
 *
 * - 'null' string, if the 'value' resolves as 'null' or 'undefined'
 * - escaped result of 'value.toString()', if the 'value' isn't a string
 * - escaped string version, if 'value' is a string.
 *
 *  The result is not escaped, if 'raw' was passed in as 'true'.
 */
text: (value, raw) => {
    value = resolveFunc(value);
    if (isNull(value)) {
...
```



# <a name="apidoc.module.pg-promise.errors.PreparedStatementError"></a>[module pg-promise.errors.PreparedStatementError](#apidoc.module.pg-promise.errors.PreparedStatementError)

#### <a name="apidoc.element.pg-promise.errors.PreparedStatementError.PreparedStatementError"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.</span>PreparedStatementError (error, ps)](#apidoc.element.pg-promise.errors.PreparedStatementError.PreparedStatementError)
- description and source-code
```javascript
function PreparedStatementError(error, ps) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'PreparedStatementError';
    this.stack = temp.stack;
    if (error instanceof $npm.QueryFileError) {
        this.error = error;
        this.message = 'Failed to initialize \'text\' from a QueryFile.';
    } else {
        this.message = error;
    }
    this.result = ps;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg-promise.errors.PreparedStatementError.prototype"></a>[module pg-promise.errors.PreparedStatementError.prototype](#apidoc.module.pg-promise.errors.PreparedStatementError.prototype)

#### <a name="apidoc.element.pg-promise.errors.PreparedStatementError.prototype.inspect"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.PreparedStatementError.prototype.</span>inspect ()](#apidoc.element.pg-promise.errors.PreparedStatementError.prototype.inspect)
- description and source-code
```javascript
inspect = function () {
    return this.toString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.errors.PreparedStatementError.prototype.toString"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.PreparedStatementError.prototype.</span>toString (level)](#apidoc.element.pg-promise.errors.PreparedStatementError.prototype.toString)
- description and source-code
```javascript
toString = function (level) {
    level = level > 0 ? parseInt(level) : 0;
    var gap0 = $npm.utils.messageGap(level),
        gap1 = $npm.utils.messageGap(level + 1),
        gap2 = $npm.utils.messageGap(level + 2),
        lines = [
            'PreparedStatementError {',
            gap1 + 'message: "' + this.message + '"',
            gap1 + 'result: {',
            gap2 + 'name: ' + JSON.stringify(this.result.name),
            gap2 + 'text: ' + JSON.stringify(this.result.text),
            gap2 + 'values: ' + JSON.stringify(this.result.values),
            gap1 + '}'
        ];
    if (this.error) {
        lines.push(gap1 + 'error: ' + this.error.toString(level + 1));
    }
    lines.push(gap0 + '}');
    return lines.join($npm.os.EOL);
}
```
- example usage
```shell
...
 *
 * @param {boolean} [raw=false]
 * Indicates when not to escape the resulting text.
 *
 * @returns {string}
 *
 * - 'null' string, if the 'value' resolves as 'null' or 'undefined'
 * - escaped result of 'value.toString()', if the 'value' isn't a string
 * - escaped string version, if 'value' is a string.
 *
 *  The result is not escaped, if 'raw' was passed in as 'true'.
 */
text: (value, raw) => {
    value = resolveFunc(value);
    if (isNull(value)) {
...
```



# <a name="apidoc.module.pg-promise.errors.QueryFileError"></a>[module pg-promise.errors.QueryFileError](#apidoc.module.pg-promise.errors.QueryFileError)

#### <a name="apidoc.element.pg-promise.errors.QueryFileError.QueryFileError"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.</span>QueryFileError (error, qf)](#apidoc.element.pg-promise.errors.QueryFileError.QueryFileError)
- description and source-code
```javascript
function QueryFileError(error, qf) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'QueryFileError';
    this.stack = temp.stack;
    if (error instanceof $npm.minify.SQLParsingError) {
        this.error = error;
        this.message = 'Failed to parse the SQL.';
    } else {
        this.message = error.message;
    }
    this.file = qf.file;
    this.options = qf.options;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg-promise.errors.QueryFileError.prototype"></a>[module pg-promise.errors.QueryFileError.prototype](#apidoc.module.pg-promise.errors.QueryFileError.prototype)

#### <a name="apidoc.element.pg-promise.errors.QueryFileError.prototype.inspect"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.QueryFileError.prototype.</span>inspect ()](#apidoc.element.pg-promise.errors.QueryFileError.prototype.inspect)
- description and source-code
```javascript
inspect = function () {
    return this.toString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.errors.QueryFileError.prototype.toString"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.QueryFileError.prototype.</span>toString (level)](#apidoc.element.pg-promise.errors.QueryFileError.prototype.toString)
- description and source-code
```javascript
toString = function (level) {
    level = level > 0 ? parseInt(level) : 0;
    var gap0 = $npm.utils.messageGap(level),
        gap1 = $npm.utils.messageGap(level + 1),
        lines = [
            'QueryFileError {',
            gap1 + 'message: "' + this.message + '"',
            gap1 + 'options: ' + JSON.stringify(this.options),
            gap1 + 'file: "' + this.file + '"'
        ];
    if (this.error) {
        lines.push(gap1 + 'error: ' + this.error.toString(level + 1));
    }
    lines.push(gap0 + '}');
    return lines.join($npm.os.EOL);
}
```
- example usage
```shell
...
 *
 * @param {boolean} [raw=false]
 * Indicates when not to escape the resulting text.
 *
 * @returns {string}
 *
 * - 'null' string, if the 'value' resolves as 'null' or 'undefined'
 * - escaped result of 'value.toString()', if the 'value' isn't a string
 * - escaped string version, if 'value' is a string.
 *
 *  The result is not escaped, if 'raw' was passed in as 'true'.
 */
text: (value, raw) => {
    value = resolveFunc(value);
    if (isNull(value)) {
...
```



# <a name="apidoc.module.pg-promise.errors.QueryResultError"></a>[module pg-promise.errors.QueryResultError](#apidoc.module.pg-promise.errors.QueryResultError)

#### <a name="apidoc.element.pg-promise.errors.QueryResultError.QueryResultError"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.</span>QueryResultError (code, result, query, values)](#apidoc.element.pg-promise.errors.QueryResultError.QueryResultError)
- description and source-code
```javascript
function QueryResultError(code, result, query, values) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'QueryResultError';
    this.stack = temp.stack;
    this.message = errorMessages[code].message;
    this.code = code;
    this.result = result;
    this.query = query;
    this.values = values;
    this.received = result.rows.length;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg-promise.errors.QueryResultError.prototype"></a>[module pg-promise.errors.QueryResultError.prototype](#apidoc.module.pg-promise.errors.QueryResultError.prototype)

#### <a name="apidoc.element.pg-promise.errors.QueryResultError.prototype.inspect"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.QueryResultError.prototype.</span>inspect ()](#apidoc.element.pg-promise.errors.QueryResultError.prototype.inspect)
- description and source-code
```javascript
inspect = function () {
    return this.toString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.errors.QueryResultError.prototype.toString"></a>[function <span class="apidocSignatureSpan">pg-promise.errors.QueryResultError.prototype.</span>toString (level)](#apidoc.element.pg-promise.errors.QueryResultError.prototype.toString)
- description and source-code
```javascript
toString = function (level) {
    level = level > 0 ? parseInt(level) : 0;
    var gap0 = $npm.utils.messageGap(level),
        gap1 = $npm.utils.messageGap(level + 1),
        lines = [
            'QueryResultError {',
            gap1 + 'code: queryResultErrorCode.' + errorMessages[this.code].name,
            gap1 + 'message: "' + this.message + '"',
            gap1 + 'received: ' + this.received,
            gap1 + 'query: ' + (typeof this.query === 'string' ? '"' + this.query + '"' : JSON.stringify(this.query))
        ];
    if (this.values !== undefined) {
        lines.push(gap1 + 'values: ' + JSON.stringify(this.values));
    }
    lines.push(gap0 + '}');
    return lines.join($npm.os.EOL);
}
```
- example usage
```shell
...
 *
 * @param {boolean} [raw=false]
 * Indicates when not to escape the resulting text.
 *
 * @returns {string}
 *
 * - 'null' string, if the 'value' resolves as 'null' or 'undefined'
 * - escaped result of 'value.toString()', if the 'value' isn't a string
 * - escaped string version, if 'value' is a string.
 *
 *  The result is not escaped, if 'raw' was passed in as 'true'.
 */
text: (value, raw) => {
    value = resolveFunc(value);
    if (isNull(value)) {
...
```



# <a name="apidoc.module.pg-promise.events"></a>[module pg-promise.events](#apidoc.module.pg-promise.events)

#### <a name="apidoc.element.pg-promise.events.connect"></a>[function <span class="apidocSignatureSpan">pg-promise.events.</span>connect (ctx, client, isFresh)](#apidoc.element.pg-promise.events.connect)
- description and source-code
```javascript
(ctx, client, isFresh) => {
    if (typeof ctx.options.connect === 'function') {
        try {
            ctx.options.connect(client, ctx.dc, isFresh);
        } catch (e) {
            // have to silence errors here;
            // cannot allow unhandled errors while connecting to the database,
            // as it will break the connection logic;
            $events.unexpected('connect', e);
        }
    }
}
```
- example usage
```shell
...
con: require('manakin').local,
utils: require('./utils'),
events: require('./events')
};

function poolConnect(ctx, config) {
return config.promise((resolve, reject) => {
    config.pgp.pg.connect(ctx.cn, (err, client, done) => {
        if (err) {
            $npm.events.error(ctx.options, err, {
                cn: $npm.utils.getSafeConnection(ctx.cn),
                dc: ctx.dc
            });
            reject(err);
        } else {
...
```

#### <a name="apidoc.element.pg-promise.events.disconnect"></a>[function <span class="apidocSignatureSpan">pg-promise.events.</span>disconnect (ctx, client)](#apidoc.element.pg-promise.events.disconnect)
- description and source-code
```javascript
(ctx, client) => {
    if (typeof ctx.options.disconnect === 'function') {
        try {
            ctx.options.disconnect(client, ctx.dc);
        } catch (e) {
            // have to silence errors here;
            // cannot allow unhandled errors while disconnecting from the database,
            // as it will break the disconnection logic;
            $events.unexpected('disconnect', e);
        }
    }
}
```
- example usage
```shell
...
                var end = lockClientEnd(client);
                resolve({
                    isFresh: isFresh,
                    client: client,
                    done: () => {
                        client.end = end;
                        done();
                        $npm.events.disconnect(ctx, client);
                    }
                });
                $npm.events.connect(ctx, client, isFresh);
            }
        });
    });
}
...
```

#### <a name="apidoc.element.pg-promise.events.error"></a>[function <span class="apidocSignatureSpan">pg-promise.events.</span>error (options, err, context)](#apidoc.element.pg-promise.events.error)
- description and source-code
```javascript
(options, err, context) => {
    if (typeof options.error === 'function') {
        try {
            options.error(err, context);
        } catch (e) {
            // have to silence errors here;
            // throwing unhandled errors while handling an error
            // notification is simply not acceptable.
            $events.unexpected('error', e);
        }
    }
}
```
- example usage
```shell
...
events: require('./events')
};

function poolConnect(ctx, config) {
return config.promise((resolve, reject) => {
    config.pgp.pg.connect(ctx.cn, (err, client, done) => {
        if (err) {
            $npm.events.error(ctx.options, err, {
                cn: $npm.utils.getSafeConnection(ctx.cn),
                dc: ctx.dc
            });
            reject(err);
        } else {
            var isFresh = !client.$used;
            if (isFresh) {
...
```

#### <a name="apidoc.element.pg-promise.events.extend"></a>[function <span class="apidocSignatureSpan">pg-promise.events.</span>extend (options, obj, dc)](#apidoc.element.pg-promise.events.extend)
- description and source-code
```javascript
(options, obj, dc) => {
    if (typeof options.extend === 'function') {
        try {
            options.extend.call(obj, obj, dc);
        } catch (e) {
            // have to silence errors here;
            // the result of throwing unhandled errors while
            // extending the protocol would be unpredictable.
            $events.unexpected('extend', e);
        }
    }
}
```
- example usage
```shell
...
        }

        // lock all default properties to read-only,
        // to prevent override by the client.
        $npm.utils.lock(obj, false, ctx.options);

        // extend the protocol;
        $npm.events.extend(ctx.options, obj, ctx.dc);

        // freeze the protocol permanently;
        $npm.utils.lock(obj, true, ctx.options);
    }

}
...
```

#### <a name="apidoc.element.pg-promise.events.query"></a>[function <span class="apidocSignatureSpan">pg-promise.events.</span>query (options, context)](#apidoc.element.pg-promise.events.query)
- description and source-code
```javascript
(options, context) => {
    if (typeof options.query === 'function') {
        try {
            options.query(context);
        } catch (e) {
            // throwing an error during event 'query'
            // will result in a reject for the request.
            return e instanceof Error ? e : new $npm.utils.InternalError(e);
        }
    }
}
```
- example usage
```shell
...
    any: 6
};
'''

In the following generic-query example we indicate that the call can return anything:

'''js
db.query('select * from users');
'''

which is equivalent to making one of the following calls:

'''js
var qrm = pgp.queryResult;
db.query('SELECT * FROM users', undefined, qrm.many | qrm.none);
...
```

#### <a name="apidoc.element.pg-promise.events.receive"></a>[function <span class="apidocSignatureSpan">pg-promise.events.</span>receive (options, data, result, context)](#apidoc.element.pg-promise.events.receive)
- description and source-code
```javascript
(options, data, result, context) => {
    if (typeof options.receive === 'function') {
        try {
            options.receive(data, result, context);
        } catch (e) {
            // throwing an error during event 'receive'
            // will result in a reject for the request.
            return e instanceof Error ? e : new $npm.utils.InternalError(e);
        }
    }
}
```
- example usage
```shell
...
 *         }
 *     }
 * }
 */
receive: (options, data, result, context) => {
    if (typeof options.receive === 'function') {
        try {
            options.receive(data, result, context);
        } catch (e) {
            // throwing an error during event 'receive'
            // will result in a reject for the request.
            return e instanceof Error ? e : new $npm.utils.InternalError(e);
        }
    }
},
...
```

#### <a name="apidoc.element.pg-promise.events.task"></a>[function <span class="apidocSignatureSpan">pg-promise.events.</span>task (options, context)](#apidoc.element.pg-promise.events.task)
- description and source-code
```javascript
(options, context) => {
    if (typeof options.task === 'function') {
        try {
            options.task(context);
        } catch (e) {
            // silencing the error, to avoid breaking the task;
            $events.unexpected('task', e);
        }
    }
}
```
- example usage
```shell
...
## Tasks

A task represents a shared connection to be used within a callback function. The callback can be either a regular function or an
 ES6 generator.

A transaction, for example, is just a special type of task, wrapped in 'CONNECT->COMMIT/ROLLBACK'.

'''js
db.task(t => {
// execute a chain of queries;
})
.then(data => {
    // success;
})
.catch(error => {
    // failed;
...
```

#### <a name="apidoc.element.pg-promise.events.transact"></a>[function <span class="apidocSignatureSpan">pg-promise.events.</span>transact (options, context)](#apidoc.element.pg-promise.events.transact)
- description and source-code
```javascript
(options, context) => {
    if (typeof options.transact === 'function') {
        try {
            options.transact(context);
        } catch (e) {
            // silencing the error, to avoid breaking the transaction;
            $events.unexpected('transact', e);
        }
    }
}
```
- example usage
```shell
...
 *     }
 * };
 *
 */
transact: (options, context) => {
    if (typeof options.transact === 'function') {
        try {
            options.transact(context);
        } catch (e) {
            // silencing the error, to avoid breaking the transaction;
            $events.unexpected('transact', e);
        }
    }
},
...
```

#### <a name="apidoc.element.pg-promise.events.unexpected"></a>[function <span class="apidocSignatureSpan">pg-promise.events.</span>unexpected (event, e)](#apidoc.element.pg-promise.events.unexpected)
- description and source-code
```javascript
(event, e) => {
    // If you should ever get here, your app is definitely broken, and you need to fix
    // your event handler to prevent unhandled errors during event notifications.
    //
    // Console output is suppressed when running tests, to avoid polluting test output
    // with error messages that are intentional and of no value to the test.

    /* istanbul ignore if */
    if (!$npm.main.suppressErrors) {
        var stack = e instanceof Error ? e.stack : new Error().stack;
        $npm.con.error('Unexpected error in \'%s\' event handler.\n%s\n', event, stack);
    }
}
```
- example usage
```shell
...
    if (typeof ctx.options.connect === 'function') {
        try {
            ctx.options.connect(client, ctx.dc, isFresh);
        } catch (e) {
            // have to silence errors here;
            // cannot allow unhandled errors while connecting to the database,
            // as it will break the connection logic;
            $events.unexpected('connect', e);
        }
    }
},

/**
 * @event disconnect
 * @description
...
```



# <a name="apidoc.module.pg-promise.formatting"></a>[module pg-promise.formatting](#apidoc.module.pg-promise.formatting)

#### <a name="apidoc.element.pg-promise.formatting.formatFunction"></a>[function <span class="apidocSignatureSpan">pg-promise.formatting.</span>formatFunction (funcName, values, capSQL)](#apidoc.element.pg-promise.formatting.formatFunction)
- description and source-code
```javascript
function $formatFunction(funcName, values, capSQL) {
    var sql = capSQL ? 'SELECT * FROM ' : 'select * from ';
    return sql + funcName + '(' + formatCSV(values) + ')';
}
```
- example usage
```shell
...
    }
}

if (!error && (!pgFormatting || isFunc)) {
    try {
        // use 'pg-promise' implementation of values formatting;
        if (isFunc) {
            query = $npm.formatting.formatFunction(query, values, capSQL);
        } else {
            query = $npm.formatting.formatQuery(query, values);
        }
    } catch (e) {
        if (isFunc) {
            var prefix = capSQL ? 'SELECT * FROM' : 'select * from';
            query = prefix + ' ' + query + '(...)';
...
```

#### <a name="apidoc.element.pg-promise.formatting.formatQuery"></a>[function <span class="apidocSignatureSpan">pg-promise.formatting.</span>formatQuery (query, values, raw, options)](#apidoc.element.pg-promise.formatting.formatQuery)
- description and source-code
```javascript
function $formatQuery(query, values, raw, options) {
    if (typeof query !== 'string') {
        throw new TypeError('Parameter \'query\' must be a text string.');
    }
    if (values && typeof values === 'object') {
        var ctf = values['formatDBType']; // custom type formatting;
        if (typeof ctf === 'function') {
            return $formatQuery(query, resolveFunc(ctf, values), raw || values._rawDBType, options);
        }
        if (values instanceof Array) {
            // $1, $2,... formatting to be applied;
            return formatAs.array(query, values, raw, options);
        }
        if (!(values instanceof Date || values instanceof Buffer)) {
            // $*propName* formatting to be applied;
            return formatAs.object(query, values, raw, options);
        }
    }
    // $1 formatting to be applied, if values != undefined;
    return values === undefined ? query : formatAs.value(query, values, raw);
}
```
- example usage
```shell
...

    if (!error && (!pgFormatting || isFunc)) {
try {
    // use 'pg-promise' implementation of values formatting;
    if (isFunc) {
        query = $npm.formatting.formatFunction(query, values, capSQL);
    } else {
        query = $npm.formatting.formatQuery(query, values);
    }
} catch (e) {
    if (isFunc) {
        var prefix = capSQL ? 'SELECT * FROM' : 'select * from';
        query = prefix + ' ' + query + '(...)';
    }
    error = e instanceof Error ? e : new $npm.utils.InternalError(e);
...
```



# <a name="apidoc.module.pg-promise.minify"></a>[module pg-promise.minify](#apidoc.module.pg-promise.minify)

#### <a name="apidoc.element.pg-promise.minify.minify"></a>[function <span class="apidocSignatureSpan">pg-promise.</span>minify (sql, options)](#apidoc.element.pg-promise.minify.minify)
- description and source-code
```javascript
function minify(sql, options) {

    if (typeof sql !== 'string') {
        throw new TypeError("Input SQL must be a text string.");
    }

    if (options !== undefined && typeof options !== 'object') {
        throw new TypeError("Parameter 'options' must be an object.");
    }

    if (!sql.length) {
        return '';
    }

    var idx = 0, // current index
        result = '', // resulting sql
        len = sql.length, // sql length
        EOL = getEOL(sql), // end-of-line
        space = false, // add a space on the next step
        compress = options && options.compress; // option 'compress'

    do {
        var s = sql[idx], // current symbol;
            s1 = idx < len - 1 ? sql[idx + 1] : ''; // next symbol;

        if (isGap(s)) {
            while (++idx < len && isGap(sql[idx]));
            if (idx < len) {
                space = true;
            }
            idx--;
            continue;
        }

        if (s === '-' && s1 === '-') {
            var lb = sql.indexOf(EOL, idx + 2);
            if (lb < 0) {
                break;
            }
            idx = lb - 1;
            skipGaps();
            continue;
        }

        if (s === '/' && s1 === '*') {
            var end = sql.indexOf('*/', idx + 2);
            if (end < 0) {
                throwError(PEC.unclosedMLC);
            }
            idx = end + 1;
            skipGaps();
            continue;
        }

        if (s === '"') {
            var closeIdx = sql.indexOf('"', idx + 1);
            if (closeIdx < 0) {
                throwError(PEC.unclosedQI);
            }
            var text = sql.substr(idx, closeIdx - idx + 1);
            if (text.indexOf(EOL) > 0) {
                throwError(PEC.multiLineQI);
            }
            if (compress) {
                space = false;
            }
            addSpace();
            result += text;
            idx = closeIdx;
            skipGaps();
            continue;
        }

        if (s === '\'') {
            var closeIdx = idx;
            do {
                closeIdx = sql.indexOf('\'', closeIdx + 1);
                if (closeIdx > 0) {
                    var step = closeIdx;
                    while (++step < len && sql[step] === '\'');
                    if ((step - closeIdx) % 2) {
                        closeIdx = step - 1;
                        break;
                    }
                    closeIdx = step === len ? -1 : step;
                }
            } while (closeIdx > 0);
            if (closeIdx < 0) {
                throwError(PEC.unclosedText);
            }
            if (compress) {
                space = false;
            }
            addSpace();
            var text = sql.substr(idx, closeIdx - idx + 1);
            var hasLB = text.indexOf(EOL) > 0;
            if (hasLB) {
                text = text.split(EOL).map(function (m) {
                    return m.replace(/^\s+|\s+$/g, '');
                }).join('\\n');
            }
            var hasTabs = text.indexOf('\t') > 0;
            if (hasLB || hasTabs) {
                var prev = idx ? sql[idx - 1] : '';
                if (prev !== 'E' && prev !== 'e') {
                    var r = result ? result[result.length - 1] : '';
                    if (r && r !== ' ' && compressors.indexOf(r) < 0) {
                        result += ' ';
                    }
                    result += 'E';
                }
                if (hasTabs) {
                    text = text.replace(/\t/g, '\\t');
                }
            }
            result += text;
            idx = closeIdx;
            skipGaps();
            continue;
        }

        if (compress && compressors.indexOf(s) >= 0) {
            space = false;
            skipGaps();
        }

        addSpace();
        result += s;

    } while (++idx < len);

    return result;

    function skipGaps() {
        if (compress) {
            while (idx < len - 1 && isGap(sql[id ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.minify.SQLParsingError"></a>[function <span class="apidocSignatureSpan">pg-promise.minify.</span>SQLParsingError (code, position)](#apidoc.element.pg-promise.minify.SQLParsingError)
- description and source-code
```javascript
function SQLParsingError(code, position) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'SQLParsingError';
    this.stack = temp.stack;
    this.code = code; // one of parsingErrorCode values;
    this.error = errorMessages[code].message;
    this.position = position; // Error position in the text: {line, column}
    this.message = "Error parsing SQL at {line:" + position.line + ",col:" + position.column + "}: " + this.error;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg-promise.minify.SQLParsingError"></a>[module pg-promise.minify.SQLParsingError](#apidoc.module.pg-promise.minify.SQLParsingError)

#### <a name="apidoc.element.pg-promise.minify.SQLParsingError.SQLParsingError"></a>[function <span class="apidocSignatureSpan">pg-promise.minify.</span>SQLParsingError (code, position)](#apidoc.element.pg-promise.minify.SQLParsingError.SQLParsingError)
- description and source-code
```javascript
function SQLParsingError(code, position) {
    var temp = Error.apply(this, arguments);
    temp.name = this.name = 'SQLParsingError';
    this.stack = temp.stack;
    this.code = code; // one of parsingErrorCode values;
    this.error = errorMessages[code].message;
    this.position = position; // Error position in the text: {line, column}
    this.message = "Error parsing SQL at {line:" + position.line + ",col:" + position.column + "}: " + this.error;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg-promise.minify.SQLParsingError.prototype"></a>[module pg-promise.minify.SQLParsingError.prototype](#apidoc.module.pg-promise.minify.SQLParsingError.prototype)

#### <a name="apidoc.element.pg-promise.minify.SQLParsingError.prototype.inspect"></a>[function <span class="apidocSignatureSpan">pg-promise.minify.SQLParsingError.prototype.</span>inspect ()](#apidoc.element.pg-promise.minify.SQLParsingError.prototype.inspect)
- description and source-code
```javascript
inspect = function () {
    return this.toString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.minify.SQLParsingError.prototype.toString"></a>[function <span class="apidocSignatureSpan">pg-promise.minify.SQLParsingError.prototype.</span>toString (level)](#apidoc.element.pg-promise.minify.SQLParsingError.prototype.toString)
- description and source-code
```javascript
toString = function (level) {
    level = level > 0 ? parseInt(level) : 0;
    var gap = messageGap(level + 1);
    var lines = [
        'SQLParsingError {',
        gap + 'code: parsingErrorCode.' + errorMessages[this.code].name,
        gap + 'error: "' + this.error + '"',
        gap + 'position: {line: ' + this.position.line + ", col: " + this.position.column + '}',
        messageGap(level) + '}'
    ];
    return lines.join(EOL);
}
```
- example usage
```shell
...
 *
 * @param {boolean} [raw=false]
 * Indicates when not to escape the resulting text.
 *
 * @returns {string}
 *
 * - 'null' string, if the 'value' resolves as 'null' or 'undefined'
 * - escaped result of 'value.toString()', if the 'value' isn't a string
 * - escaped string version, if 'value' is a string.
 *
 *  The result is not escaped, if 'raw' was passed in as 'true'.
 */
text: (value, raw) => {
    value = resolveFunc(value);
    if (isNull(value)) {
...
```



# <a name="apidoc.module.pg-promise.special"></a>[module pg-promise.special](#apidoc.module.pg-promise.special)

#### <a name="apidoc.element.pg-promise.special.SpecialQuery"></a>[function <span class="apidocSignatureSpan">pg-promise.special.</span>SpecialQuery (type)](#apidoc.element.pg-promise.special.SpecialQuery)
- description and source-code
```javascript
function SpecialQuery(type) {
    this.isStream = type === 'stream';
    this.isResult = type === 'result';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg-promise.txMode"></a>[module pg-promise.txMode](#apidoc.module.pg-promise.txMode)

#### <a name="apidoc.element.pg-promise.txMode.TransactionMode"></a>[function <span class="apidocSignatureSpan">pg-promise.txMode.</span>TransactionMode (tiLevel, readOnly, deferrable)](#apidoc.element.pg-promise.txMode.TransactionMode)
- description and source-code
```javascript
function TransactionMode(tiLevel, readOnly, deferrable) {

    if (!(this instanceof TransactionMode)) {
        return new TransactionMode(tiLevel, readOnly, deferrable);
    }

    if (tiLevel && typeof tiLevel === 'object') {
        readOnly = tiLevel.readOnly;
        deferrable = tiLevel.deferrable;
        tiLevel = tiLevel.tiLevel;
    }

    var level, accessMode, deferrableMode, capBegin, begin = 'begin';

    tiLevel = (tiLevel > 0) ? parseInt(tiLevel) : 0;

    if (tiLevel > 0 && tiLevel < 4) {
        var values = ['serializable', 'repeatable read', 'read committed'];
        level = 'isolation level ' + values[tiLevel - 1];
    }

    if (readOnly) {
        accessMode = 'read only';
    } else {
        if (readOnly !== undefined) {
            accessMode = 'read write';
        }
    }

    // From the official documentation: http://www.postgresql.org/docs/9.5/static/sql-set-transaction.html
    // The DEFERRABLE transaction property has no effect unless the transaction is also SERIALIZABLE and READ ONLY
    if (tiLevel === isolationLevel.serializable && readOnly) {
        if (deferrable) {
            deferrableMode = 'deferrable';
        } else {
            if (deferrable !== undefined) {
                deferrableMode = 'not deferrable';
            }
        }
    }

    if (level) {
        begin += ' ' + level;
    }

    if (accessMode) {
        begin += ' ' + accessMode;
    }

    if (deferrableMode) {
        begin += ' ' + deferrableMode;
    }

    capBegin = begin.toUpperCase();

    this.begin = cap => {
        return cap ? capBegin : begin;
    };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg-promise.utils"></a>[module pg-promise.utils](#apidoc.module.pg-promise.utils)

#### <a name="apidoc.element.pg-promise.utils.buildSqlModule"></a>[function <span class="apidocSignatureSpan">pg-promise.utils.</span>buildSqlModule (config)](#apidoc.element.pg-promise.utils.buildSqlModule)
- description and source-code
```javascript
function buildSqlModule(config) {

    if ($npm.utils.isText(config)) {
        var path = $npm.utils.isPathAbsolute(config) ? config : $npm.path.join($npm.utils.startDir, config);
        config = require(path);
    } else {
        if ($npm.utils.isNull(config)) {
            var defConfig = $npm.path.join($npm.utils.startDir, 'sql-config.json');
            // istanbul ignore else;
            if (!$npm.fs.existsSync(defConfig)) {
                throw new Error('Default SQL configuration file not found: ' + defConfig);
            }
            // cannot test this automatically, because it requires that file 'sql-config.json'
            // resides within the Jasmine folder, since it is the client during the test.
            // istanbul ignore next;
            config = require(defConfig);
        } else {
            if (!config || typeof config !== 'object') {
                throw new TypeError('Invalid parameter \'config\' specified.');
            }
        }
    }

    if (!$npm.utils.isText(config.dir)) {
        throw new Error('Property \'dir\' must be a non-empty string.');
    }

    var total = 0;

    var tree = enumSql(config.dir, {recursive: config.recursive, ignoreErrors: config.ignoreErrors}, () => {
        total++;
    });

    var modulePath = './loadSql', moduleName = 'load';
    if (config.module && typeof config.module === 'object') {
        if ($npm.utils.isText(config.module.path)) {
            modulePath = config.module.path;
        }
        if ($npm.utils.isText(config.module.name)) {
            moduleName = config.module.name;
        }
    }

    var d = new Date();

    var header =
        '/////////////////////////////////////////////////////////////////////////' + EOL +
        '// This file was automatically generated by pg-promise v.' + $npm.package.version + EOL +
        '//' + EOL +
        '// Generated on: ' + d.toLocaleDateString() + ', at ' + d.toLocaleTimeString() + EOL +
        '// Total files: ' + total + EOL +
        '//' + EOL +
        '// API: http://vitaly-t.github.io/pg-promise/utils.html#.buildSqlModule' + EOL +
        '/////////////////////////////////////////////////////////////////////////' + EOL + EOL +
        '\'use strict\';' + EOL + EOL +
        'var ' + moduleName + ' = require(\'' + modulePath + '\');' + EOL + EOL +
        'module.exports = ';

    var code = header + objectToCode(tree, value => {
            return moduleName + '(' + JSON.stringify(value) + ')';
        }) + ';';

    if ($npm.utils.isText(config.output)) {
        var p = config.output;
        if (!$npm.utils.isPathAbsolute(p)) {
            p = $npm.path.join($npm.utils.startDir, p);
        }
        $npm.fs.writeFileSync(p, code);
    }

    return code;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.utils.camelize"></a>[function <span class="apidocSignatureSpan">pg-promise.utils.</span>camelize (text)](#apidoc.element.pg-promise.utils.camelize)
- description and source-code
```javascript
function camelize(text) {
    text = text.replace(/[\-_\s\.]+(.)?/g, (match, chr) => {
        return chr ? chr.toUpperCase() : '';
    });
    return text.substr(0, 1).toLowerCase() + text.substr(1);
}
```
- example usage
```shell
...
*         camelizeColumns(data);
*     }
* };
*
* function camelizeColumns(data) {
*     var template = data[0];
*     for (var prop in template) {
*         var camel = pgp.utils.camelize(prop);
*         if (!(camel in template)) {
*             for (var i = 0; i < data.length; i++) {
*                 var d = data[i];
*                 d[camel] = d[prop];
*                 delete d[prop];
*             }
*         }
...
```

#### <a name="apidoc.element.pg-promise.utils.camelizeVar"></a>[function <span class="apidocSignatureSpan">pg-promise.utils.</span>camelizeVar (text)](#apidoc.element.pg-promise.utils.camelizeVar)
- description and source-code
```javascript
function camelizeVar(text) {
    text = text.replace(/[^a-zA-Z0-9\$_\-\s\.]/g, '').replace(/^[0-9_\-\s\.]+/, '');
    return camelize(text);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.utils.enumSql"></a>[function <span class="apidocSignatureSpan">pg-promise.utils.</span>enumSql (dir, options, cb)](#apidoc.element.pg-promise.utils.enumSql)
- description and source-code
```javascript
function enumSql(dir, options, cb) {
    if (!$npm.utils.isText(dir)) {
        throw new TypeError('Parameter \'dir\' must be a non-empty text string.');
    }
    if (!options || typeof options !== 'object') {
        options = {};
    }
    cb = (typeof cb === 'function') ? cb : null;
    return _enumSql(dir, options, cb, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg-promise.utils.objectToCode"></a>[function <span class="apidocSignatureSpan">pg-promise.utils.</span>objectToCode (obj, cb)](#apidoc.element.pg-promise.utils.objectToCode)
- description and source-code
```javascript
function objectToCode(obj, cb) {

    if (!obj || typeof obj !== 'object') {
        throw new TypeError('Parameter \'obj\' must be a non-null object.');
    }

    cb = (typeof cb === 'function') ? cb : null;

    return '{' + generate(obj, 1) + EOL + '}';

    function generate(obj, level) {
        var code = '', gap = $npm.utils.messageGap(level);
        var idx = 0;
        for (var prop in obj) {
            var value = obj[prop];
            if (idx) {
                code += ',';
            }
            if (value && typeof value === 'object') {
                code += EOL + gap + prop + ': {';
                code += generate(value, level + 1);
                code += EOL + gap + '}';
            } else {
                code += EOL + gap + prop + ': ';
                if (cb) {
                    code += cb(value, prop, obj);
                } else {
                    code += JSON.stringify(value);
                }
            }
            idx++;
        }
        return code;
    }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
