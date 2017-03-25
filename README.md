# api documentation for  [pg (v6.1.5)](http://github.com/brianc/node-postgres)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-pg.svg)](https://travis-ci.org/npmdoc/node-npmdoc-pg)
#### PostgreSQL client - pure javascript & libpq with the same API

[![NPM](https://nodei.co/npm/pg.png?downloads=true)](https://www.npmjs.com/package/pg)

[![apidoc](https://npmdoc.github.io/node-npmdoc-pg/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-pg_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-pg/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-pg/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Brian Carlson",
        "email": "brian.m.carlson@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/brianc/node-postgres/issues"
    },
    "dependencies": {
        "buffer-writer": "1.0.1",
        "packet-reader": "0.2.0",
        "pg-connection-string": "0.1.3",
        "pg-pool": "1.*",
        "pg-types": "1.*",
        "pgpass": "1.x",
        "semver": "4.3.2"
    },
    "description": "PostgreSQL client - pure javascript & libpq with the same API",
    "devDependencies": {
        "async": "0.9.0",
        "co": "4.6.0",
        "jshint": "2.5.2",
        "lodash": "4.13.1",
        "pg-copy-streams": "0.3.0",
        "promise-polyfill": "5.2.1"
    },
    "directories": {},
    "dist": {
        "shasum": "204fa40c1252ab7220d7cf6992886b20d77862b8",
        "tarball": "https://registry.npmjs.org/pg/-/pg-6.1.5.tgz"
    },
    "engines": {
        "node": ">= 0.8.0"
    },
    "gitHead": "3de22ba991676534b366144c02145c015cca6125",
    "homepage": "http://github.com/brianc/node-postgres",
    "keywords": [
        "postgres",
        "pg",
        "libpq",
        "postgre",
        "database",
        "rdbms"
    ],
    "license": "MIT",
    "main": "./lib",
    "maintainers": [
        {
            "name": "brianc",
            "email": "brian.m.carlson@gmail.com"
        }
    ],
    "minNativeVersion": "1.7.0",
    "name": "pg",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/brianc/node-postgres.git"
    },
    "scripts": {
        "changelog": "npm i github-changes && ./node_modules/.bin/github-changes -o brianc -r node-postgres -d pulls -a -v",
        "test": "make test-all connectionString=postgres://postgres@localhost:5432/postgres"
    },
    "version": "6.1.5"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module pg](#apidoc.module.pg)
1.  [function <span class="apidocSignatureSpan">pg.</span>Client (config)](#apidoc.element.pg.Client)
1.  [function <span class="apidocSignatureSpan">pg.</span>Connection (config)](#apidoc.element.pg.Connection)
1.  [function <span class="apidocSignatureSpan">pg.</span>Pool (options)](#apidoc.element.pg.Pool)
1.  [function <span class="apidocSignatureSpan">pg.</span>Pool.super_ (options, Client)](#apidoc.element.pg.Pool.super_)
1.  [function <span class="apidocSignatureSpan">pg.</span>Query (config, values, callback)](#apidoc.element.pg.Query)
1.  [function <span class="apidocSignatureSpan">pg.</span>connection_parameters (config)](#apidoc.element.pg.connection_parameters)
1.  [function <span class="apidocSignatureSpan">pg.</span>result (rowMode)](#apidoc.element.pg.result)
1.  [function <span class="apidocSignatureSpan">pg.</span>type_overrides (userTypes)](#apidoc.element.pg.type_overrides)
1.  number <span class="apidocSignatureSpan">pg.</span>_eventsCount
1.  object <span class="apidocSignatureSpan">pg.</span>Client.prototype
1.  object <span class="apidocSignatureSpan">pg.</span>Connection.prototype
1.  object <span class="apidocSignatureSpan">pg.</span>Pool.super_.prototype
1.  object <span class="apidocSignatureSpan">pg.</span>Query.prototype
1.  object <span class="apidocSignatureSpan">pg.</span>_events
1.  object <span class="apidocSignatureSpan">pg.</span>_pools
1.  object <span class="apidocSignatureSpan">pg.</span>connection_parameters.prototype
1.  object <span class="apidocSignatureSpan">pg.</span>defaults
1.  object <span class="apidocSignatureSpan">pg.</span>domain
1.  object <span class="apidocSignatureSpan">pg.</span>native
1.  object <span class="apidocSignatureSpan">pg.</span>result.prototype
1.  object <span class="apidocSignatureSpan">pg.</span>type_overrides.prototype
1.  object <span class="apidocSignatureSpan">pg.</span>types
1.  object <span class="apidocSignatureSpan">pg.</span>types.arrayParser
1.  object <span class="apidocSignatureSpan">pg.</span>utils

#### [module pg.Client](#apidoc.module.pg.Client)
1.  [function <span class="apidocSignatureSpan">pg.</span>Client (config)](#apidoc.element.pg.Client.Client)
1.  [function <span class="apidocSignatureSpan">pg.Client.</span>Query (config, values, callback)](#apidoc.element.pg.Client.Query)
1.  [function <span class="apidocSignatureSpan">pg.Client.</span>md5 (string)](#apidoc.element.pg.Client.md5)
1.  [function <span class="apidocSignatureSpan">pg.Client.</span>super_ ()](#apidoc.element.pg.Client.super_)

#### [module pg.Client.prototype](#apidoc.module.pg.Client.prototype)
1.  [function <span class="apidocSignatureSpan">pg.Client.prototype.</span>_pulseQueryQueue ()](#apidoc.element.pg.Client.prototype._pulseQueryQueue)
1.  [function <span class="apidocSignatureSpan">pg.Client.prototype.</span>cancel (client, query)](#apidoc.element.pg.Client.prototype.cancel)
1.  [function <span class="apidocSignatureSpan">pg.Client.prototype.</span>connect (callback)](#apidoc.element.pg.Client.prototype.connect)
1.  [function <span class="apidocSignatureSpan">pg.Client.prototype.</span>copyFrom (text)](#apidoc.element.pg.Client.prototype.copyFrom)
1.  [function <span class="apidocSignatureSpan">pg.Client.prototype.</span>copyTo (text)](#apidoc.element.pg.Client.prototype.copyTo)
1.  [function <span class="apidocSignatureSpan">pg.Client.prototype.</span>end (cb)](#apidoc.element.pg.Client.prototype.end)
1.  [function <span class="apidocSignatureSpan">pg.Client.prototype.</span>escapeIdentifier (str)](#apidoc.element.pg.Client.prototype.escapeIdentifier)
1.  [function <span class="apidocSignatureSpan">pg.Client.prototype.</span>escapeLiteral (str)](#apidoc.element.pg.Client.prototype.escapeLiteral)
1.  [function <span class="apidocSignatureSpan">pg.Client.prototype.</span>getStartupConf ()](#apidoc.element.pg.Client.prototype.getStartupConf)
1.  [function <span class="apidocSignatureSpan">pg.Client.prototype.</span>getTypeParser (oid, format)](#apidoc.element.pg.Client.prototype.getTypeParser)
1.  [function <span class="apidocSignatureSpan">pg.Client.prototype.</span>query (config, values, callback)](#apidoc.element.pg.Client.prototype.query)
1.  [function <span class="apidocSignatureSpan">pg.Client.prototype.</span>setTypeParser (oid, format, parseFn)](#apidoc.element.pg.Client.prototype.setTypeParser)

#### [module pg.Connection](#apidoc.module.pg.Connection)
1.  [function <span class="apidocSignatureSpan">pg.</span>Connection (config)](#apidoc.element.pg.Connection.Connection)
1.  [function <span class="apidocSignatureSpan">pg.Connection.</span>super_ ()](#apidoc.element.pg.Connection.super_)

#### [module pg.Connection.prototype](#apidoc.module.pg.Connection.prototype)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>_readValue (buffer)](#apidoc.element.pg.Connection.prototype._readValue)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>_send (code, more)](#apidoc.element.pg.Connection.prototype._send)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>attachListeners (stream)](#apidoc.element.pg.Connection.prototype.attachListeners)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>bind (config, more)](#apidoc.element.pg.Connection.prototype.bind)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>cancel (processID, secretKey)](#apidoc.element.pg.Connection.prototype.cancel)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>close (msg, more)](#apidoc.element.pg.Connection.prototype.close)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>connect (port, host)](#apidoc.element.pg.Connection.prototype.connect)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>describe (msg, more)](#apidoc.element.pg.Connection.prototype.describe)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>end ()](#apidoc.element.pg.Connection.prototype.end)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>endCopyFrom ()](#apidoc.element.pg.Connection.prototype.endCopyFrom)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>execute (config, more)](#apidoc.element.pg.Connection.prototype.execute)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>flush ()](#apidoc.element.pg.Connection.prototype.flush)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parse (query, more)](#apidoc.element.pg.Connection.prototype.parse)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseA (buffer, length)](#apidoc.element.pg.Connection.prototype.parseA)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseC (buffer, length)](#apidoc.element.pg.Connection.prototype.parseC)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseCString (buffer)](#apidoc.element.pg.Connection.prototype.parseCString)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseD (buffer, length)](#apidoc.element.pg.Connection.prototype.parseD)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseE (buffer, length)](#apidoc.element.pg.Connection.prototype.parseE)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseField (buffer)](#apidoc.element.pg.Connection.prototype.parseField)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseG (buffer, length)](#apidoc.element.pg.Connection.prototype.parseG)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseGH (buffer, msg)](#apidoc.element.pg.Connection.prototype.parseGH)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseH (buffer, length)](#apidoc.element.pg.Connection.prototype.parseH)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseInt16 (buffer)](#apidoc.element.pg.Connection.prototype.parseInt16)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseInt32 (buffer)](#apidoc.element.pg.Connection.prototype.parseInt32)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseK (buffer, length)](#apidoc.element.pg.Connection.prototype.parseK)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseMessage (buffer)](#apidoc.element.pg.Connection.prototype.parseMessage)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseN (buffer, length)](#apidoc.element.pg.Connection.prototype.parseN)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseR (buffer, length)](#apidoc.element.pg.Connection.prototype.parseR)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseS (buffer, length)](#apidoc.element.pg.Connection.prototype.parseS)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseT (buffer, length)](#apidoc.element.pg.Connection.prototype.parseT)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseZ (buffer, length)](#apidoc.element.pg.Connection.prototype.parseZ)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parsed (buffer, length)](#apidoc.element.pg.Connection.prototype.parsed)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>password (password)](#apidoc.element.pg.Connection.prototype.password)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>query (text)](#apidoc.element.pg.Connection.prototype.query)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>readBytes (buffer, length)](#apidoc.element.pg.Connection.prototype.readBytes)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>readString (buffer, length)](#apidoc.element.pg.Connection.prototype.readString)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>requestSsl ()](#apidoc.element.pg.Connection.prototype.requestSsl)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>sendCopyFail (msg)](#apidoc.element.pg.Connection.prototype.sendCopyFail)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>sendCopyFromChunk (chunk)](#apidoc.element.pg.Connection.prototype.sendCopyFromChunk)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>startup (config)](#apidoc.element.pg.Connection.prototype.startup)
1.  [function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>sync ()](#apidoc.element.pg.Connection.prototype.sync)

#### [module pg.Pool](#apidoc.module.pg.Pool)
1.  [function <span class="apidocSignatureSpan">pg.</span>Pool (options)](#apidoc.element.pg.Pool.Pool)
1.  [function <span class="apidocSignatureSpan">pg.Pool.</span>super_ (options, Client)](#apidoc.element.pg.Pool.super_)

#### [module pg.Pool.super_](#apidoc.module.pg.Pool.super_)
1.  [function <span class="apidocSignatureSpan">pg.Pool.</span>super_ ()](#apidoc.element.pg.Pool.super_.super_)

#### [module pg.Pool.super_.prototype](#apidoc.module.pg.Pool.super_.prototype)
1.  [function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>_create (cb)](#apidoc.element.pg.Pool.super_.prototype._create)
1.  [function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>_destroy (client)](#apidoc.element.pg.Pool.super_.prototype._destroy)
1.  [function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>_promise (cb, executor)](#apidoc.element.pg.Pool.super_.prototype._promise)
1.  [function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>_promiseNoCallback (callback, executor)](#apidoc.element.pg.Pool.super_.prototype._promiseNoCallback)
1.  [function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>connect (cb)](#apidoc.element.pg.Pool.super_.prototype.connect)
1.  [function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>end (cb)](#apidoc.element.pg.Pool.super_.prototype.end)
1.  [function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>query (text, values, cb)](#apidoc.element.pg.Pool.super_.prototype.query)
1.  [function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>take (cb)](#apidoc.element.pg.Pool.super_.prototype.take)

#### [module pg.Query](#apidoc.module.pg.Query)
1.  [function <span class="apidocSignatureSpan">pg.</span>Query (config, values, callback)](#apidoc.element.pg.Query.Query)
1.  [function <span class="apidocSignatureSpan">pg.Query.</span>super_ ()](#apidoc.element.pg.Query.super_)

#### [module pg.Query.prototype](#apidoc.module.pg.Query.prototype)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>_getRows (connection, rows)](#apidoc.element.pg.Query.prototype._getRows)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>catch (callback)](#apidoc.element.pg.Query.prototype.catch)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleCommandComplete (msg, con)](#apidoc.element.pg.Query.prototype.handleCommandComplete)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleCopyData (msg, connection)](#apidoc.element.pg.Query.prototype.handleCopyData)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleCopyInResponse (connection)](#apidoc.element.pg.Query.prototype.handleCopyInResponse)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleDataRow (msg)](#apidoc.element.pg.Query.prototype.handleDataRow)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleEmptyQuery (con)](#apidoc.element.pg.Query.prototype.handleEmptyQuery)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleError (err, connection)](#apidoc.element.pg.Query.prototype.handleError)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handlePortalSuspended (connection)](#apidoc.element.pg.Query.prototype.handlePortalSuspended)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleReadyForQuery (con)](#apidoc.element.pg.Query.prototype.handleReadyForQuery)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleRowDescription (msg)](#apidoc.element.pg.Query.prototype.handleRowDescription)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>hasBeenParsed (connection)](#apidoc.element.pg.Query.prototype.hasBeenParsed)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>prepare (connection)](#apidoc.element.pg.Query.prototype.prepare)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>promise ()](#apidoc.element.pg.Query.prototype.promise)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>requiresPreparation ()](#apidoc.element.pg.Query.prototype.requiresPreparation)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>submit (connection)](#apidoc.element.pg.Query.prototype.submit)
1.  [function <span class="apidocSignatureSpan">pg.Query.prototype.</span>then (onSuccess, onFailure)](#apidoc.element.pg.Query.prototype.then)

#### [module pg.connection_parameters](#apidoc.module.pg.connection_parameters)
1.  [function <span class="apidocSignatureSpan">pg.</span>connection_parameters (config)](#apidoc.element.pg.connection_parameters.connection_parameters)

#### [module pg.connection_parameters.prototype](#apidoc.module.pg.connection_parameters.prototype)
1.  [function <span class="apidocSignatureSpan">pg.connection_parameters.prototype.</span>getLibpqConnectionString (cb)](#apidoc.element.pg.connection_parameters.prototype.getLibpqConnectionString)

#### [module pg.result](#apidoc.module.pg.result)
1.  [function <span class="apidocSignatureSpan">pg.</span>result (rowMode)](#apidoc.element.pg.result.result)

#### [module pg.result.prototype](#apidoc.module.pg.result.prototype)
1.  [function <span class="apidocSignatureSpan">pg.result.prototype.</span>_getTypeParser (oid, format)](#apidoc.element.pg.result.prototype._getTypeParser)
1.  [function <span class="apidocSignatureSpan">pg.result.prototype.</span>_parseRowAsArray (rowData)](#apidoc.element.pg.result.prototype._parseRowAsArray)
1.  [function <span class="apidocSignatureSpan">pg.result.prototype.</span>addCommandComplete (msg)](#apidoc.element.pg.result.prototype.addCommandComplete)
1.  [function <span class="apidocSignatureSpan">pg.result.prototype.</span>addFields (fieldDescriptions)](#apidoc.element.pg.result.prototype.addFields)
1.  [function <span class="apidocSignatureSpan">pg.result.prototype.</span>addRow (row)](#apidoc.element.pg.result.prototype.addRow)
1.  [function <span class="apidocSignatureSpan">pg.result.prototype.</span>parseRow (rowData)](#apidoc.element.pg.result.prototype.parseRow)

#### [module pg.type_overrides](#apidoc.module.pg.type_overrides)
1.  [function <span class="apidocSignatureSpan">pg.</span>type_overrides (userTypes)](#apidoc.element.pg.type_overrides.type_overrides)

#### [module pg.type_overrides.prototype](#apidoc.module.pg.type_overrides.prototype)
1.  [function <span class="apidocSignatureSpan">pg.type_overrides.prototype.</span>getOverrides (format)](#apidoc.element.pg.type_overrides.prototype.getOverrides)
1.  [function <span class="apidocSignatureSpan">pg.type_overrides.prototype.</span>getTypeParser (oid, format)](#apidoc.element.pg.type_overrides.prototype.getTypeParser)
1.  [function <span class="apidocSignatureSpan">pg.type_overrides.prototype.</span>setTypeParser (oid, format, parseFn)](#apidoc.element.pg.type_overrides.prototype.setTypeParser)

#### [module pg.types](#apidoc.module.pg.types)
1.  [function <span class="apidocSignatureSpan">pg.types.</span>getTypeParser (oid, format)](#apidoc.element.pg.types.getTypeParser)
1.  [function <span class="apidocSignatureSpan">pg.types.</span>setTypeParser (oid, format, parseFn)](#apidoc.element.pg.types.setTypeParser)
1.  object <span class="apidocSignatureSpan">pg.types.</span>arrayParser

#### [module pg.types.arrayParser](#apidoc.module.pg.types.arrayParser)
1.  [function <span class="apidocSignatureSpan">pg.types.arrayParser.</span>create (source, transform)](#apidoc.element.pg.types.arrayParser.create)

#### [module pg.utils](#apidoc.module.pg.utils)
1.  [function <span class="apidocSignatureSpan">pg.utils.</span>normalizeQueryConfig (config, values, callback)](#apidoc.element.pg.utils.normalizeQueryConfig)
1.  [function <span class="apidocSignatureSpan">pg.utils.</span>prepareValue (value)](#apidoc.element.pg.utils.prepareValue)



# <a name="apidoc.module.pg"></a>[module pg](#apidoc.module.pg)

#### <a name="apidoc.element.pg.Client"></a>[function <span class="apidocSignatureSpan">pg.</span>Client (config)](#apidoc.element.pg.Client)
- description and source-code
```javascript
Client = function (config) {
  EventEmitter.call(this);

  this.connectionParameters = new ConnectionParameters(config);
  this.user = this.connectionParameters.user;
  this.database = this.connectionParameters.database;
  this.port = this.connectionParameters.port;
  this.host = this.connectionParameters.host;
  this.password = this.connectionParameters.password;

  var c = config || {};

  this._types = new TypeOverrides(c.types);

  this.connection = c.connection || new Connection({
    stream: c.stream,
    ssl: this.connectionParameters.ssl,
    keepAlive: c.keepAlive || false
  });
  this.queryQueue = [];
  this.binary = c.binary || defaults.binary;
  this.encoding = 'utf8';
  this.processID = null;
  this.secretKey = null;
  this.ssl = this.connectionParameters.ssl || false;
}
```
- example usage
```shell
...

'''js
var pg = require('pg');

// instantiate a new client
// the client will read connection information from
// the same environment variables used by postgres cli tools
var client = new pg.Client();

// connect to our database
client.connect(function (err) {
if (err) throw err;

// execute a query on our database
client.query('SELECT $1::text as name', ['brianc'], function (err, result) {
...
```

#### <a name="apidoc.element.pg.Connection"></a>[function <span class="apidocSignatureSpan">pg.</span>Connection (config)](#apidoc.element.pg.Connection)
- description and source-code
```javascript
Connection = function (config) {
  EventEmitter.call(this);
  config = config || {};
  this.stream = config.stream || new net.Stream();
  this._keepAlive = config.keepAlive;
  this.lastBuffer = false;
  this.lastOffset = 0;
  this.buffer = null;
  this.offset = null;
  this.encoding = 'utf8';
  this.parsedStatements = {};
  this.writer = new Writer();
  this.ssl = config.ssl || false;
  this._ending = false;
  this._mode = TEXT_MODE;
  this._emitMessage = false;
  this._reader = new Reader({
    headerSize: 1,
    lengthPadding: -4
  });
  var self = this;
  this.on('newListener', function(eventName) {
    if(eventName == 'message') {
      self._emitMessage = true;
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Pool"></a>[function <span class="apidocSignatureSpan">pg.</span>Pool (options)](#apidoc.element.pg.Pool)
- description and source-code
```javascript
Pool = function (options) {
  var config = { Client: Client };
  for (var key in options) {
    config[key] = options[key];
  }
  Pool.call(this, config);
}
```
- example usage
```shell
...
idleTimeoutMillis: 30000, // how long a client is allowed to remain idle before being closed
};


//this initializes a connection pool
//it will keep idle connections open for 30 seconds
//and set a limit of maximum 10 idle clients
var pool = new pg.Pool(config);

// to run a query we can acquire a client from the pool,
// run a query on the client, and then return the client to the pool
pool.connect(function(err, client, done) {
if(err) {
  return console.error('error fetching client from pool', err);
}
...
```

#### <a name="apidoc.element.pg.Pool.super_"></a>[function <span class="apidocSignatureSpan">pg.</span>Pool.super_ (options, Client)](#apidoc.element.pg.Pool.super_)
- description and source-code
```javascript
Pool.super_ = function (options, Client) {
  if (!(this instanceof Pool)) {
    return new Pool(options, Client)
  }
  EventEmitter.call(this)
  this.options = objectAssign({}, options)
  this.log = this.options.log || function () { }
  this.Client = this.options.Client || Client || require('pg').Client
  this.Promise = this.options.Promise || Promise

  this.options.max = this.options.max || this.options.poolSize || 10
  this.options.create = this.options.create || this._create.bind(this)
  this.options.destroy = this.options.destroy || this._destroy.bind(this)
  this.pool = new genericPool.Pool(this.options)
  this.onCreate = this.options.onCreate
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query"></a>[function <span class="apidocSignatureSpan">pg.</span>Query (config, values, callback)](#apidoc.element.pg.Query)
- description and source-code
```javascript
Query = function (config, values, callback) {
  // use of "new" optional
  if(!(this instanceof Query)) { return new Query(config, values, callback); }

  config = utils.normalizeQueryConfig(config, values, callback);

  this.text = config.text;
  this.values = config.values;
  this.rows = config.rows;
  this.types = config.types;
  this.name = config.name;
  this.binary = config.binary;
  this.stream = config.stream;
  //use unique portal name each time
  this.portal = config.portal || "";
  this.callback = config.callback;
  if(process.domain && config.callback) {
    this.callback = process.domain.bind(config.callback);
  }
  this._result = new Result(config.rowMode, config.types);
  this.isPreparedStatement = false;
  this._canceledDueToError = false;
  this._promise = null;
  EventEmitter.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.connection_parameters"></a>[function <span class="apidocSignatureSpan">pg.</span>connection_parameters (config)](#apidoc.element.pg.connection_parameters)
- description and source-code
```javascript
connection_parameters = function (config) {
  //if a string is passed, it is a raw connection string so we parse it into a config
  config = typeof config == 'string' ? parse(config) : (config || {});
  //if the config has a connectionString defined, parse IT into the config we use
  //this will override other default values with what is stored in connectionString
  if(config.connectionString) {
    config = parse(config.connectionString);
  }
  this.user = val('user', config);
  this.database = val('database', config);
  this.port = parseInt(val('port', config), 10);
  this.host = val('host', config);
  this.password = val('password', config);
  this.binary = val('binary', config);
  this.ssl = typeof config.ssl === 'undefined' ? useSsl() : config.ssl;
  this.client_encoding = val("client_encoding", config);
  //a domain socket begins with '/'
  this.isDomainSocket = (!(this.host||'').indexOf('/'));

  this.application_name = val('application_name', config, 'PGAPPNAME');
  this.fallback_application_name = val('fallback_application_name', config, false);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.result"></a>[function <span class="apidocSignatureSpan">pg.</span>result (rowMode)](#apidoc.element.pg.result)
- description and source-code
```javascript
result = function (rowMode) {
  this.command = null;
  this.rowCount = null;
  this.oid = null;
  this.rows = [];
  this.fields = [];
  this._parsers = [];
  this.RowCtor = null;
  this.rowAsArray = rowMode == "array";
  if(this.rowAsArray) {
    this.parseRow = this._parseRowAsArray;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.type_overrides"></a>[function <span class="apidocSignatureSpan">pg.</span>type_overrides (userTypes)](#apidoc.element.pg.type_overrides)
- description and source-code
```javascript
function TypeOverrides(userTypes) {
  this._types = userTypes || types;
  this.text = {};
  this.binary = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.Client"></a>[module pg.Client](#apidoc.module.pg.Client)

#### <a name="apidoc.element.pg.Client.Client"></a>[function <span class="apidocSignatureSpan">pg.</span>Client (config)](#apidoc.element.pg.Client.Client)
- description and source-code
```javascript
Client = function (config) {
  EventEmitter.call(this);

  this.connectionParameters = new ConnectionParameters(config);
  this.user = this.connectionParameters.user;
  this.database = this.connectionParameters.database;
  this.port = this.connectionParameters.port;
  this.host = this.connectionParameters.host;
  this.password = this.connectionParameters.password;

  var c = config || {};

  this._types = new TypeOverrides(c.types);

  this.connection = c.connection || new Connection({
    stream: c.stream,
    ssl: this.connectionParameters.ssl,
    keepAlive: c.keepAlive || false
  });
  this.queryQueue = [];
  this.binary = c.binary || defaults.binary;
  this.encoding = 'utf8';
  this.processID = null;
  this.secretKey = null;
  this.ssl = this.connectionParameters.ssl || false;
}
```
- example usage
```shell
...

'''js
var pg = require('pg');

// instantiate a new client
// the client will read connection information from
// the same environment variables used by postgres cli tools
var client = new pg.Client();

// connect to our database
client.connect(function (err) {
if (err) throw err;

// execute a query on our database
client.query('SELECT $1::text as name', ['brianc'], function (err, result) {
...
```

#### <a name="apidoc.element.pg.Client.Query"></a>[function <span class="apidocSignatureSpan">pg.Client.</span>Query (config, values, callback)](#apidoc.element.pg.Client.Query)
- description and source-code
```javascript
Query = function (config, values, callback) {
  // use of "new" optional
  if(!(this instanceof Query)) { return new Query(config, values, callback); }

  config = utils.normalizeQueryConfig(config, values, callback);

  this.text = config.text;
  this.values = config.values;
  this.rows = config.rows;
  this.types = config.types;
  this.name = config.name;
  this.binary = config.binary;
  this.stream = config.stream;
  //use unique portal name each time
  this.portal = config.portal || "";
  this.callback = config.callback;
  if(process.domain && config.callback) {
    this.callback = process.domain.bind(config.callback);
  }
  this._result = new Result(config.rowMode, config.types);
  this.isPreparedStatement = false;
  this._canceledDueToError = false;
  this._promise = null;
  EventEmitter.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Client.md5"></a>[function <span class="apidocSignatureSpan">pg.Client.</span>md5 (string)](#apidoc.element.pg.Client.md5)
- description and source-code
```javascript
md5 = function (string) {
  return crypto.createHash('md5').update(string, 'utf-8').digest('hex');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Client.super_"></a>[function <span class="apidocSignatureSpan">pg.Client.</span>super_ ()](#apidoc.element.pg.Client.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.Client.prototype"></a>[module pg.Client.prototype](#apidoc.module.pg.Client.prototype)

#### <a name="apidoc.element.pg.Client.prototype._pulseQueryQueue"></a>[function <span class="apidocSignatureSpan">pg.Client.prototype.</span>_pulseQueryQueue ()](#apidoc.element.pg.Client.prototype._pulseQueryQueue)
- description and source-code
```javascript
_pulseQueryQueue = function () {
  if(this.readyForQuery===true) {
    this.activeQuery = this.queryQueue.shift();
    if(this.activeQuery) {
      this.readyForQuery = false;
      this.hasExecuted = true;
      this.activeQuery.submit(this.connection);
    } else if(this.hasExecuted) {
      this.activeQuery = null;
      this.emit('drain');
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Client.prototype.cancel"></a>[function <span class="apidocSignatureSpan">pg.Client.prototype.</span>cancel (client, query)](#apidoc.element.pg.Client.prototype.cancel)
- description and source-code
```javascript
cancel = function (client, query) {
  if(client.activeQuery == query) {
    var con = this.connection;

    if(this.host && this.host.indexOf('/') === 0) {
      con.connect(this.host + '/.s.PGSQL.' + this.port);
    } else {
      con.connect(this.port, this.host);
    }

    //once connection is established send cancel message
    con.on('connect', function() {
      con.cancel(client.processID, client.secretKey);
    });
  } else if(client.queryQueue.indexOf(query) != -1) {
    client.queryQueue.splice(client.queryQueue.indexOf(query), 1);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Client.prototype.connect"></a>[function <span class="apidocSignatureSpan">pg.Client.prototype.</span>connect (callback)](#apidoc.element.pg.Client.prototype.connect)
- description and source-code
```javascript
connect = function (callback) {
  var self = this;
  var con = this.connection;

  if(this.host && this.host.indexOf('/') === 0) {
    con.connect(this.host + '/.s.PGSQL.' + this.port);
  } else {
    con.connect(this.port, this.host);
  }


  //once connection is established send startup message
  con.on('connect', function() {
    if(self.ssl) {
      con.requestSsl();
    } else {
      con.startup(self.getStartupConf());
    }
  });

  con.on('sslconnect', function() {
    con.startup(self.getStartupConf());
  });

  function checkPgPass(cb) {
    return function(msg) {
      if (null !== self.password) {
        cb(msg);
      } else {
        pgPass(self.connectionParameters, function(pass){
          if (undefined !== pass) {
            self.connectionParameters.password = self.password = pass;
          }
          cb(msg);
        });
      }
    };
  }

  //password request handling
  con.on('authenticationCleartextPassword', checkPgPass(function() {
    con.password(self.password);
  }));

  //password request handling
  con.on('authenticationMD5Password', checkPgPass(function(msg) {
    var inner = Client.md5(self.password + self.user);
    var outer = Client.md5(Buffer.concat([new Buffer(inner), msg.salt]));
    var md5password = "md5" + outer;
    con.password(md5password);
  }));

  con.once('backendKeyData', function(msg) {
    self.processID = msg.processID;
    self.secretKey = msg.secretKey;
  });

  //hook up query handling events to connection
  //after the connection initially becomes ready for queries
  con.once('readyForQuery', function() {

    //delegate rowDescription to active query
    con.on('rowDescription', function(msg) {
      self.activeQuery.handleRowDescription(msg);
    });

    //delegate dataRow to active query
    con.on('dataRow', function(msg) {
      self.activeQuery.handleDataRow(msg);
    });

    //delegate portalSuspended to active query
    con.on('portalSuspended', function(msg) {
      self.activeQuery.handlePortalSuspended(con);
    });

    //deletagate emptyQuery to active query
    con.on('emptyQuery', function(msg) {
      self.activeQuery.handleEmptyQuery(con);
    });

    //delegate commandComplete to active query
    con.on('commandComplete', function(msg) {
      self.activeQuery.handleCommandComplete(msg, con);
    });

    //if a prepared statement has a name and properly parses
    //we track that its already been executed so we don't parse
    //it again on the same client
    con.on('parseComplete', function(msg) {
      if(self.activeQuery.name) {
        con.parsedStatements[self.activeQuery.name] = true;
      }
    });

    con.on('copyInResponse', function(msg) {
      self.activeQuery.handleCopyInResponse(self.connection);
    });

    con.on('copyData', function (msg) {
      self.activeQuery.handleCopyData(msg, self.connection);
    });

    con.on('notification', function(msg) {
      self.emit('notification', msg);
    });

    //process possible callback argument to Client#connect
    if (callback) {
      callback(null, self);
      //remove callback for proper error handling
      //after the connect event
      callback = null;
    }
    self.emit('connect');
  });

  con.on('readyForQuery', function() {
    var activeQuery = self.activeQuery;
    self.activeQuery = null;
    self.readyForQuery = true;
    self._pulseQueryQueue();
    if(activeQuery) {
      activeQuery.handleReadyForQuery(con);
    }
  });

  con.on('error', function(error) {
    if(self.activeQuery) {
      var activeQuery = self.activeQuery;
      self.activeQuery = null;
      return activeQuery.handleError(error, con);
    }
    if(!callback) {
      return self.emit('error', error);
    }
    con.end(); // make sure ECONNRESET errors don't cause error events
    callback(error);
    callback = null;
  });

  con.once('end', function() {
    if ( callback ) {
      // haven't received a connection message yet !
      var err = new Error('Connection terminated');
      callback(err);
      callback = null;
      return;
    }
    if(self.activeQuery) {
      var disconnectError = ...
```
- example usage
```shell
...

// instantiate a new client
// the client will read connection information from
// the same environment variables used by postgres cli tools
var client = new pg.Client();

// connect to our database
client.connect(function (err) {
  if (err) throw err;

  // execute a query on our database
  client.query('SELECT $1::text as name', ['brianc'], function (err, result) {
if (err) throw err;

// just print the result to the console
...
```

#### <a name="apidoc.element.pg.Client.prototype.copyFrom"></a>[function <span class="apidocSignatureSpan">pg.Client.prototype.</span>copyFrom (text)](#apidoc.element.pg.Client.prototype.copyFrom)
- description and source-code
```javascript
copyFrom = function (text) {
  throw new Error("For PostgreSQL COPY TO/COPY FROM support npm install pg-copy-streams");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Client.prototype.copyTo"></a>[function <span class="apidocSignatureSpan">pg.Client.prototype.</span>copyTo (text)](#apidoc.element.pg.Client.prototype.copyTo)
- description and source-code
```javascript
copyTo = function (text) {
  throw new Error("For PostgreSQL COPY TO/COPY FROM support npm install pg-copy-streams");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Client.prototype.end"></a>[function <span class="apidocSignatureSpan">pg.Client.prototype.</span>end (cb)](#apidoc.element.pg.Client.prototype.end)
- description and source-code
```javascript
end = function (cb) {
  this.connection.end();
  if (cb) {
    this.connection.once('end', cb);
  }
}
```
- example usage
```shell
...
  client.query('SELECT $1::text as name', ['brianc'], function (err, result) {
    if (err) throw err;

    // just print the result to the console
    console.log(result.rows[0]); // outputs: { name: 'brianc' }

    // disconnect the client
    client.end(function (err) {
      if (err) throw err;
    });
  });
});

'''
...
```

#### <a name="apidoc.element.pg.Client.prototype.escapeIdentifier"></a>[function <span class="apidocSignatureSpan">pg.Client.prototype.</span>escapeIdentifier (str)](#apidoc.element.pg.Client.prototype.escapeIdentifier)
- description and source-code
```javascript
escapeIdentifier = function (str) {

  var escaped = '"';

  for(var i = 0; i < str.length; i++) {
    var c = str[i];
    if(c === '"') {
      escaped += c + c;
    } else {
      escaped += c;
    }
  }

  escaped += '"';

  return escaped;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Client.prototype.escapeLiteral"></a>[function <span class="apidocSignatureSpan">pg.Client.prototype.</span>escapeLiteral (str)](#apidoc.element.pg.Client.prototype.escapeLiteral)
- description and source-code
```javascript
escapeLiteral = function (str) {

  var hasBackslash = false;
  var escaped = '\'';

  for(var i = 0; i < str.length; i++) {
    var c = str[i];
    if(c === '\'') {
      escaped += c + c;
    } else if (c === '\\') {
      escaped += c + c;
      hasBackslash = true;
    } else {
      escaped += c;
    }
  }

  escaped += '\'';

  if(hasBackslash === true) {
    escaped = ' E' + escaped;
  }

  return escaped;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Client.prototype.getStartupConf"></a>[function <span class="apidocSignatureSpan">pg.Client.prototype.</span>getStartupConf ()](#apidoc.element.pg.Client.prototype.getStartupConf)
- description and source-code
```javascript
getStartupConf = function () {
  var params = this.connectionParameters;

  var data = {
    user: params.user,
    database: params.database
  };

  var appName = params.application_name || params.fallback_application_name;
  if (appName) {
    data.application_name = appName;
  }

  return data;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Client.prototype.getTypeParser"></a>[function <span class="apidocSignatureSpan">pg.Client.prototype.</span>getTypeParser (oid, format)](#apidoc.element.pg.Client.prototype.getTypeParser)
- description and source-code
```javascript
getTypeParser = function (oid, format) {
  return this._types.getTypeParser(oid, format);
}
```
- example usage
```shell
...
  fallback_application_name: undefined,

  parseInputDatesAsUTC: false
};

var pgTypes = require('pg-types');
// save default parsers
var parseBigInteger = pgTypes.getTypeParser(20, 'text');
var parseBigIntegerArray = pgTypes.getTypeParser(1016, 'text');

//parse int8 so you can get your count values as actual numbers
module.exports.__defineSetter__("parseInt8", function(val) {
  pgTypes.setTypeParser(20, 'text', val ? pgTypes.getTypeParser(23, 'text') : parseBigInteger);
  pgTypes.setTypeParser(1016, 'text', val ? pgTypes.getTypeParser(1007, 'text') : parseBigIntegerArray);
});
...
```

#### <a name="apidoc.element.pg.Client.prototype.query"></a>[function <span class="apidocSignatureSpan">pg.Client.prototype.</span>query (config, values, callback)](#apidoc.element.pg.Client.prototype.query)
- description and source-code
```javascript
query = function (config, values, callback) {
  //can take in strings, config object or query object
  var query = (typeof config.submit == 'function') ? config :
     new Query(config, values, callback);
  if(this.binary && !query.binary) {
    query.binary = true;
  }
  if(query._result) {
    query._result._getTypeParser = this._types.getTypeParser.bind(this._types);
  }

  this.queryQueue.push(query);
  this._pulseQueryQueue();
  return query;
}
```
- example usage
```shell
...
var client = new pg.Client();

// connect to our database
client.connect(function (err) {
  if (err) throw err;

  // execute a query on our database
  client.query('SELECT $1::text as name', ['brianc'], function (err, result) {
if (err) throw err;

// just print the result to the console
console.log(result.rows[0]); // outputs: { name: 'brianc' }

// disconnect the client
client.end(function (err) {
...
```

#### <a name="apidoc.element.pg.Client.prototype.setTypeParser"></a>[function <span class="apidocSignatureSpan">pg.Client.prototype.</span>setTypeParser (oid, format, parseFn)](#apidoc.element.pg.Client.prototype.setTypeParser)
- description and source-code
```javascript
setTypeParser = function (oid, format, parseFn) {
  return this._types.setTypeParser(oid, format, parseFn);
}
```
- example usage
```shell
...
var pgTypes = require('pg-types');
// save default parsers
var parseBigInteger = pgTypes.getTypeParser(20, 'text');
var parseBigIntegerArray = pgTypes.getTypeParser(1016, 'text');

//parse int8 so you can get your count values as actual numbers
module.exports.__defineSetter__("parseInt8", function(val) {
  pgTypes.setTypeParser(20, 'text', val ? pgTypes.getTypeParser(23, 'text') : parseBigInteger);
  pgTypes.setTypeParser(1016, 'text', val ? pgTypes.getTypeParser(1007, 'text') : parseBigIntegerArray);
});
...
```



# <a name="apidoc.module.pg.Connection"></a>[module pg.Connection](#apidoc.module.pg.Connection)

#### <a name="apidoc.element.pg.Connection.Connection"></a>[function <span class="apidocSignatureSpan">pg.</span>Connection (config)](#apidoc.element.pg.Connection.Connection)
- description and source-code
```javascript
Connection = function (config) {
  EventEmitter.call(this);
  config = config || {};
  this.stream = config.stream || new net.Stream();
  this._keepAlive = config.keepAlive;
  this.lastBuffer = false;
  this.lastOffset = 0;
  this.buffer = null;
  this.offset = null;
  this.encoding = 'utf8';
  this.parsedStatements = {};
  this.writer = new Writer();
  this.ssl = config.ssl || false;
  this._ending = false;
  this._mode = TEXT_MODE;
  this._emitMessage = false;
  this._reader = new Reader({
    headerSize: 1,
    lengthPadding: -4
  });
  var self = this;
  this.on('newListener', function(eventName) {
    if(eventName == 'message') {
      self._emitMessage = true;
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.super_"></a>[function <span class="apidocSignatureSpan">pg.Connection.</span>super_ ()](#apidoc.element.pg.Connection.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.Connection.prototype"></a>[module pg.Connection.prototype](#apidoc.module.pg.Connection.prototype)

#### <a name="apidoc.element.pg.Connection.prototype._readValue"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>_readValue (buffer)](#apidoc.element.pg.Connection.prototype._readValue)
- description and source-code
```javascript
_readValue = function (buffer) {
  var length = this.parseInt32(buffer);
  if(length === -1) return null;
  if(this._mode === TEXT_MODE) {
    return this.readString(buffer, length);
  }
  return this.readBytes(buffer, length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype._send"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>_send (code, more)](#apidoc.element.pg.Connection.prototype._send)
- description and source-code
```javascript
_send = function (code, more) {
  if(!this.stream.writable) { return false; }
  if(more === true) {
    this.writer.addHeader(code);
  } else {
    return this.stream.write(this.writer.flush(code));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.attachListeners"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>attachListeners (stream)](#apidoc.element.pg.Connection.prototype.attachListeners)
- description and source-code
```javascript
attachListeners = function (stream) {
  var self = this;
  stream.on('data', function(buff) {
    self._reader.addChunk(buff);
    var packet = self._reader.read();
    while(packet) {
      var msg = self.parseMessage(packet);
      if(self._emitMessage) {
        self.emit('message', msg);
      }
      self.emit(msg.name, msg);
      packet = self._reader.read();
    }
  });
  stream.on('end', function() {
    self.emit('end');
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.bind"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>bind (config, more)](#apidoc.element.pg.Connection.prototype.bind)
- description and source-code
```javascript
bind = function (config, more) {
  //normalize config
  config = config || {};
  config.portal = config.portal || '';
  config.statement = config.statement || '';
  config.binary = config.binary || false;
  var values = config.values || [];
  var len = values.length;
  var useBinary = false;
  for (var j = 0; j < len; j++)
    useBinary |= values[j] instanceof Buffer;
  var buffer = this.writer
    .addCString(config.portal)
    .addCString(config.statement);
  if (!useBinary)
    buffer.addInt16(0);
  else {
    buffer.addInt16(len);
    for (j = 0; j < len; j++)
      buffer.addInt16(values[j] instanceof Buffer);
  }
  buffer.addInt16(len);
  for(var i = 0; i < len; i++) {
    var val = values[i];
    if(val === null || typeof val === "undefined") {
      buffer.addInt32(-1);
    } else if (val instanceof Buffer) {
      buffer.addInt32(val.length);
      buffer.add(val);
    } else {
      buffer.addInt32(Buffer.byteLength(val));
      buffer.addString(val);
    }
  }

  if(config.binary) {
    buffer.addInt16(1); // format codes to use binary
    buffer.addInt16(1);
  }
  else {
    buffer.addInt16(0); // format codes to use text
  }
  //0x42 = 'B'
  this._send(0x42, more);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.cancel"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>cancel (processID, secretKey)](#apidoc.element.pg.Connection.prototype.cancel)
- description and source-code
```javascript
cancel = function (processID, secretKey) {
  var bodyBuffer = this.writer
    .addInt16(1234)
    .addInt16(5678)
    .addInt32(processID)
    .addInt32(secretKey)
    .flush();

  var length = bodyBuffer.length + 4;

  var buffer = new Writer()
    .addInt32(length)
    .add(bodyBuffer)
    .join();
  this.stream.write(buffer);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.close"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>close (msg, more)](#apidoc.element.pg.Connection.prototype.close)
- description and source-code
```javascript
close = function (msg, more) {
  this.writer.addCString(msg.type + (msg.name || ''));
  this._send(0x43, more);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.connect"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>connect (port, host)](#apidoc.element.pg.Connection.prototype.connect)
- description and source-code
```javascript
connect = function (port, host) {

  if(this.stream.readyState === 'closed') {
    this.stream.connect(port, host);
  } else if(this.stream.readyState == 'open') {
    this.emit('connect');
  }

  var self = this;

  this.stream.on('connect', function() {
    if (self._keepAlive) {
      self.stream.setKeepAlive(true);
    }
    self.emit('connect');
  });

  this.stream.on('error', function(error) {
    //don't raise ECONNRESET errors - they can & should be ignored
    //during disconnect
    if(self._ending && error.code == 'ECONNRESET') {
      return;
    }
    self.emit('error', error);
  });

  this.stream.on('close', function() {
    // NOTE: node-0.10 emits both 'end' and 'close'
    //       for streams closed by the peer, while
    //       node-0.8 only emits 'close'
    self.emit('end');
  });

  if(!this.ssl) {
    return this.attachListeners(this.stream);
  }

  this.stream.once('data', function(buffer) {
    var responseCode = buffer.toString('utf8');
    if(responseCode != 'S') {
      return self.emit('error', new Error('The server does not support SSL connections'));
    }
    var tls = require('tls');
    self.stream = tls.connect({
      socket: self.stream,
      servername: host,
      rejectUnauthorized: self.ssl.rejectUnauthorized,
      ca: self.ssl.ca,
      pfx: self.ssl.pfx,
      key: self.ssl.key,
      passphrase: self.ssl.passphrase,
      cert: self.ssl.cert,
      NPNProtocols: self.ssl.NPNProtocols
    });
    self.attachListeners(self.stream);
    self.emit('sslconnect');

    self.stream.on('error', function(error){
      self.emit('error', error);
    });
  });
}
```
- example usage
```shell
...

// instantiate a new client
// the client will read connection information from
// the same environment variables used by postgres cli tools
var client = new pg.Client();

// connect to our database
client.connect(function (err) {
  if (err) throw err;

  // execute a query on our database
  client.query('SELECT $1::text as name', ['brianc'], function (err, result) {
if (err) throw err;

// just print the result to the console
...
```

#### <a name="apidoc.element.pg.Connection.prototype.describe"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>describe (msg, more)](#apidoc.element.pg.Connection.prototype.describe)
- description and source-code
```javascript
describe = function (msg, more) {
  this.writer.addCString(msg.type + (msg.name || ''));
  this._send(0x44, more);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.end"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>end ()](#apidoc.element.pg.Connection.prototype.end)
- description and source-code
```javascript
end = function () {
  //0x58 = 'X'
  this.writer.add(emptyBuffer);
  this._ending = true;
  this._send(0x58);
}
```
- example usage
```shell
...
  client.query('SELECT $1::text as name', ['brianc'], function (err, result) {
    if (err) throw err;

    // just print the result to the console
    console.log(result.rows[0]); // outputs: { name: 'brianc' }

    // disconnect the client
    client.end(function (err) {
      if (err) throw err;
    });
  });
});

'''
...
```

#### <a name="apidoc.element.pg.Connection.prototype.endCopyFrom"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>endCopyFrom ()](#apidoc.element.pg.Connection.prototype.endCopyFrom)
- description and source-code
```javascript
endCopyFrom = function () {
  this.stream.write(this.writer.add(emptyBuffer).flush(0x63));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.execute"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>execute (config, more)](#apidoc.element.pg.Connection.prototype.execute)
- description and source-code
```javascript
execute = function (config, more) {
  config = config || {};
  config.portal = config.portal || '';
  config.rows = config.rows || '';
  this.writer
    .addCString(config.portal)
    .addInt32(config.rows);

  //0x45 = 'E'
  this._send(0x45, more);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.flush"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>flush ()](#apidoc.element.pg.Connection.prototype.flush)
- description and source-code
```javascript
flush = function () {
  //0x48 = 'H'
  this.writer.add(emptyBuffer);
  this._send(0x48);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parse"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parse (query, more)](#apidoc.element.pg.Connection.prototype.parse)
- description and source-code
```javascript
parse = function (query, more) {
  //expect something like this:
  // { name: 'queryName',
  //   text: 'select * from blah',
  //   types: ['int8', 'bool'] }

  //normalize missing query names to allow for null
  query.name = query.name || '';
  if (query.name.length > 63) {
    console.error('Warning! Postgres only supports 63 characters for query names.');
    console.error('You supplied', query.name, '(', query.name.length, ')');
    console.error('This can cause conflicts and silent errors executing queries');
  }
  //normalize null type array
  query.types = query.types || [];
  var len = query.types.length;
  var buffer = this.writer
    .addCString(query.name) //name of query
    .addCString(query.text) //actual query text
    .addInt16(len);
  for(var i = 0; i < len; i++) {
    buffer.addInt32(query.types[i]);
  }

  var code = 0x50;
  this._send(code, more);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseA"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseA (buffer, length)](#apidoc.element.pg.Connection.prototype.parseA)
- description and source-code
```javascript
parseA = function (buffer, length) {
  var msg = new Message('notification', length);
  msg.processId = this.parseInt32(buffer);
  msg.channel = this.parseCString(buffer);
  msg.payload = this.parseCString(buffer);
  return msg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseC"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseC (buffer, length)](#apidoc.element.pg.Connection.prototype.parseC)
- description and source-code
```javascript
parseC = function (buffer, length) {
  var msg = new Message('commandComplete', length);
  msg.text = this.parseCString(buffer);
  return msg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseCString"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseCString (buffer)](#apidoc.element.pg.Connection.prototype.parseCString)
- description and source-code
```javascript
parseCString = function (buffer) {
  var start = this.offset;
  var end = indexOf(buffer, 0, start);
  this.offset = end + 1;
  return buffer.toString(this.encoding, start, end);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseD"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseD (buffer, length)](#apidoc.element.pg.Connection.prototype.parseD)
- description and source-code
```javascript
parseD = function (buffer, length) {
  var fieldCount = this.parseInt16(buffer);
  var msg = new DataRowMessage(length, fieldCount);
  for(var i = 0; i < fieldCount; i++) {
    msg.fields.push(this._readValue(buffer));
  }
  return msg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseE"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseE (buffer, length)](#apidoc.element.pg.Connection.prototype.parseE)
- description and source-code
```javascript
parseE = function (buffer, length) {
  var fields = {};
  var msg, item;
  var input = new Message('error', length);
  var fieldType = this.readString(buffer, 1);
  while(fieldType != '\0') {
    fields[fieldType] = this.parseCString(buffer);
    fieldType = this.readString(buffer, 1);
  }
  if(input.name === 'error') {
    // the msg is an Error instance
    msg = new Error(fields.M);
    for (item in input) {
      // copy input properties to the error
      if(input.hasOwnProperty(item)) {
        msg[item] = input[item];
      }
    }
  } else {
    // the msg is an object literal
    msg = input;
    msg.message = fields.M;
  }
  msg.severity = fields.S;
  msg.code = fields.C;
  msg.detail = fields.D;
  msg.hint = fields.H;
  msg.position = fields.P;
  msg.internalPosition = fields.p;
  msg.internalQuery = fields.q;
  msg.where = fields.W;
  msg.schema = fields.s;
  msg.table = fields.t;
  msg.column = fields.c;
  msg.dataType = fields.d;
  msg.constraint = fields.n;
  msg.file = fields.F;
  msg.line = fields.L;
  msg.routine = fields.R;
  return msg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseField"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseField (buffer)](#apidoc.element.pg.Connection.prototype.parseField)
- description and source-code
```javascript
parseField = function (buffer) {
  var field = new Field();
  field.name = this.parseCString(buffer);
  field.tableID = this.parseInt32(buffer);
  field.columnID = this.parseInt16(buffer);
  field.dataTypeID = this.parseInt32(buffer);
  field.dataTypeSize = this.parseInt16(buffer);
  field.dataTypeModifier = this.parseInt32(buffer);
  if(this.parseInt16(buffer) === TEXT_MODE) {
    this._mode = TEXT_MODE;
    field.format = FORMAT_TEXT;
  } else {
    this._mode = BINARY_MODE;
    field.format = FORMAT_BINARY;
  }
  return field;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseG"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseG (buffer, length)](#apidoc.element.pg.Connection.prototype.parseG)
- description and source-code
```javascript
parseG = function (buffer, length) {
  var msg = new Message('copyInResponse', length);
  return this.parseGH(buffer, msg);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseGH"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseGH (buffer, msg)](#apidoc.element.pg.Connection.prototype.parseGH)
- description and source-code
```javascript
parseGH = function (buffer, msg) {
  var isBinary = buffer[this.offset] !== 0;
  this.offset++;
  msg.binary = isBinary;
  var columnCount = this.parseInt16(buffer);
  msg.columnTypes = [];
  for(var i = 0; i<columnCount; i++) {
    msg.columnTypes.push(this.parseInt16(buffer));
  }
  return msg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseH"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseH (buffer, length)](#apidoc.element.pg.Connection.prototype.parseH)
- description and source-code
```javascript
parseH = function (buffer, length) {
  var msg = new Message('copyOutResponse', length);
  return this.parseGH(buffer, msg);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseInt16"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseInt16 (buffer)](#apidoc.element.pg.Connection.prototype.parseInt16)
- description and source-code
```javascript
parseInt16 = function (buffer) {
  var value = buffer.readInt16BE(this.offset, true);
  this.offset += 2;
  return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseInt32"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseInt32 (buffer)](#apidoc.element.pg.Connection.prototype.parseInt32)
- description and source-code
```javascript
parseInt32 = function (buffer) {
  var value = buffer.readInt32BE(this.offset, true);
  this.offset += 4;
  return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseK"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseK (buffer, length)](#apidoc.element.pg.Connection.prototype.parseK)
- description and source-code
```javascript
parseK = function (buffer, length) {
  var msg = new Message('backendKeyData', length);
  msg.processID = this.parseInt32(buffer);
  msg.secretKey = this.parseInt32(buffer);
  return msg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseMessage"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseMessage (buffer)](#apidoc.element.pg.Connection.prototype.parseMessage)
- description and source-code
```javascript
parseMessage = function (buffer) {

  this.offset = 0;
  var length = buffer.length + 4;
  switch(this._reader.header)
  {

  case 0x52: //R
    return this.parseR(buffer, length);

  case 0x53: //S
    return this.parseS(buffer, length);

  case 0x4b: //K
    return this.parseK(buffer, length);

  case 0x43: //C
    return this.parseC(buffer, length);

  case 0x5a: //Z
    return this.parseZ(buffer, length);

  case 0x54: //T
    return this.parseT(buffer, length);

  case 0x44: //D
    return this.parseD(buffer, length);

  case 0x45: //E
    return this.parseE(buffer, length);

  case 0x4e: //N
    return this.parseN(buffer, length);

  case 0x31: //1
    return new Message('parseComplete', length);

  case 0x32: //2
    return new Message('bindComplete', length);

  case 0x33: //3
    return new Message('closeComplete', length);

  case 0x41: //A
    return this.parseA(buffer, length);

  case 0x6e: //n
    return new Message('noData', length);

  case 0x49: //I
    return new Message('emptyQuery', length);

  case 0x73: //s
    return new Message('portalSuspended', length);

  case 0x47: //G
    return this.parseG(buffer, length);

  case 0x48: //H
    return this.parseH(buffer, length);

  case 0x63: //c
    return new Message('copyDone', length);

  case 0x64: //d
    return this.parsed(buffer, length);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseN"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseN (buffer, length)](#apidoc.element.pg.Connection.prototype.parseN)
- description and source-code
```javascript
parseN = function (buffer, length) {
  var msg = this.parseE(buffer, length);
  msg.name = 'notice';
  return msg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseR"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseR (buffer, length)](#apidoc.element.pg.Connection.prototype.parseR)
- description and source-code
```javascript
parseR = function (buffer, length) {
  var code = 0;
  var msg = new Message('authenticationOk', length);
  if(msg.length === 8) {
    code = this.parseInt32(buffer);
    if(code === 3) {
      msg.name = 'authenticationCleartextPassword';
    }
    return msg;
  }
  if(msg.length === 12) {
    code = this.parseInt32(buffer);
    if(code === 5) { //md5 required
      msg.name = 'authenticationMD5Password';
      msg.salt = new Buffer(4);
      buffer.copy(msg.salt, 0, this.offset, this.offset + 4);
      this.offset += 4;
      return msg;
    }
  }
  throw new Error("Unknown authenticationOk message type" + util.inspect(msg));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseS"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseS (buffer, length)](#apidoc.element.pg.Connection.prototype.parseS)
- description and source-code
```javascript
parseS = function (buffer, length) {
  var msg = new Message('parameterStatus', length);
  msg.parameterName = this.parseCString(buffer);
  msg.parameterValue = this.parseCString(buffer);
  return msg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseT"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseT (buffer, length)](#apidoc.element.pg.Connection.prototype.parseT)
- description and source-code
```javascript
parseT = function (buffer, length) {
  var msg = new Message(ROW_DESCRIPTION, length);
  msg.fieldCount = this.parseInt16(buffer);
  var fields = [];
  for(var i = 0; i < msg.fieldCount; i++){
    fields.push(this.parseField(buffer));
  }
  msg.fields = fields;
  return msg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parseZ"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parseZ (buffer, length)](#apidoc.element.pg.Connection.prototype.parseZ)
- description and source-code
```javascript
parseZ = function (buffer, length) {
  var msg = new Message('readyForQuery', length);
  msg.name = 'readyForQuery';
  msg.status = this.readString(buffer, 1);
  return msg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.parsed"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>parsed (buffer, length)](#apidoc.element.pg.Connection.prototype.parsed)
- description and source-code
```javascript
parsed = function (buffer, length) {
  var msg = new Message('copyData', length);
  msg.chunk = this.readBytes(buffer, msg.length - 4);
  return msg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.password"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>password (password)](#apidoc.element.pg.Connection.prototype.password)
- description and source-code
```javascript
password = function (password) {
  //0x70 = 'p'
  this._send(0x70, this.writer.addCString(password));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.query"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>query (text)](#apidoc.element.pg.Connection.prototype.query)
- description and source-code
```javascript
query = function (text) {
  //0x51 = Q
  this.stream.write(this.writer.addCString(text).flush(0x51));
}
```
- example usage
```shell
...
var client = new pg.Client();

// connect to our database
client.connect(function (err) {
  if (err) throw err;

  // execute a query on our database
  client.query('SELECT $1::text as name', ['brianc'], function (err, result) {
if (err) throw err;

// just print the result to the console
console.log(result.rows[0]); // outputs: { name: 'brianc' }

// disconnect the client
client.end(function (err) {
...
```

#### <a name="apidoc.element.pg.Connection.prototype.readBytes"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>readBytes (buffer, length)](#apidoc.element.pg.Connection.prototype.readBytes)
- description and source-code
```javascript
readBytes = function (buffer, length) {
  return buffer.slice(this.offset, this.offset += length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.readString"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>readString (buffer, length)](#apidoc.element.pg.Connection.prototype.readString)
- description and source-code
```javascript
readString = function (buffer, length) {
  return buffer.toString(this.encoding, this.offset, (this.offset += length));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.requestSsl"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>requestSsl ()](#apidoc.element.pg.Connection.prototype.requestSsl)
- description and source-code
```javascript
requestSsl = function () {
  this.checkSslResponse = true;

  var bodyBuffer = this.writer
    .addInt16(0x04D2)
    .addInt16(0x162F).flush();

  var length = bodyBuffer.length + 4;

  var buffer = new Writer()
    .addInt32(length)
    .add(bodyBuffer)
    .join();
  this.stream.write(buffer);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.sendCopyFail"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>sendCopyFail (msg)](#apidoc.element.pg.Connection.prototype.sendCopyFail)
- description and source-code
```javascript
sendCopyFail = function (msg) {
  //this.stream.write(this.writer.add(emptyBuffer).flush(0x66));
  this.writer.addCString(msg);
  this._send(0x66);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.sendCopyFromChunk"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>sendCopyFromChunk (chunk)](#apidoc.element.pg.Connection.prototype.sendCopyFromChunk)
- description and source-code
```javascript
sendCopyFromChunk = function (chunk) {
  this.stream.write(this.writer.add(chunk).flush(0x64));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.startup"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>startup (config)](#apidoc.element.pg.Connection.prototype.startup)
- description and source-code
```javascript
startup = function (config) {
  var writer = this.writer
    .addInt16(3)
    .addInt16(0)
  ;

  Object.keys(config).forEach(function(key){
    var val = config[key];
    writer.addCString(key).addCString(val);
  });

  writer.addCString('client_encoding').addCString("'utf-8'");

  var bodyBuffer = writer.addCString('').flush();
  //this message is sent without a code

  var length = bodyBuffer.length + 4;

  var buffer = new Writer()
    .addInt32(length)
    .add(bodyBuffer)
    .join();
  this.stream.write(buffer);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Connection.prototype.sync"></a>[function <span class="apidocSignatureSpan">pg.Connection.prototype.</span>sync ()](#apidoc.element.pg.Connection.prototype.sync)
- description and source-code
```javascript
sync = function () {
  //clear out any pending data in the writer
  this.writer.flush(0);

  this.writer.add(emptyBuffer);
  this._ending = true;
  this._send(0x53);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.Pool"></a>[module pg.Pool](#apidoc.module.pg.Pool)

#### <a name="apidoc.element.pg.Pool.Pool"></a>[function <span class="apidocSignatureSpan">pg.</span>Pool (options)](#apidoc.element.pg.Pool.Pool)
- description and source-code
```javascript
Pool = function (options) {
  var config = { Client: Client };
  for (var key in options) {
    config[key] = options[key];
  }
  Pool.call(this, config);
}
```
- example usage
```shell
...
idleTimeoutMillis: 30000, // how long a client is allowed to remain idle before being closed
};


//this initializes a connection pool
//it will keep idle connections open for 30 seconds
//and set a limit of maximum 10 idle clients
var pool = new pg.Pool(config);

// to run a query we can acquire a client from the pool,
// run a query on the client, and then return the client to the pool
pool.connect(function(err, client, done) {
if(err) {
  return console.error('error fetching client from pool', err);
}
...
```

#### <a name="apidoc.element.pg.Pool.super_"></a>[function <span class="apidocSignatureSpan">pg.Pool.</span>super_ (options, Client)](#apidoc.element.pg.Pool.super_)
- description and source-code
```javascript
super_ = function (options, Client) {
  if (!(this instanceof Pool)) {
    return new Pool(options, Client)
  }
  EventEmitter.call(this)
  this.options = objectAssign({}, options)
  this.log = this.options.log || function () { }
  this.Client = this.options.Client || Client || require('pg').Client
  this.Promise = this.options.Promise || Promise

  this.options.max = this.options.max || this.options.poolSize || 10
  this.options.create = this.options.create || this._create.bind(this)
  this.options.destroy = this.options.destroy || this._destroy.bind(this)
  this.pool = new genericPool.Pool(this.options)
  this.onCreate = this.options.onCreate
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.Pool.super_"></a>[module pg.Pool.super_](#apidoc.module.pg.Pool.super_)

#### <a name="apidoc.element.pg.Pool.super_.super_"></a>[function <span class="apidocSignatureSpan">pg.Pool.</span>super_ ()](#apidoc.element.pg.Pool.super_.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.Pool.super_.prototype"></a>[module pg.Pool.super_.prototype](#apidoc.module.pg.Pool.super_.prototype)

#### <a name="apidoc.element.pg.Pool.super_.prototype._create"></a>[function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>_create (cb)](#apidoc.element.pg.Pool.super_.prototype._create)
- description and source-code
```javascript
_create = function (cb) {
  this.log('connecting new client')
  var client = new this.Client(this.options)

  client.on('error', function (e) {
    this.log('connected client error:', e)
    this.pool.destroy(client)
    e.client = client
    this.emit('error', e)
  }.bind(this))

  client.connect(function (err) {
    if (err) {
      this.log('client connection error:', err)
      cb(err)
    } else {
      this.log('client connected')
      this.emit('connect', client)
      cb(null, client)
    }
  }.bind(this))
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Pool.super_.prototype._destroy"></a>[function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>_destroy (client)](#apidoc.element.pg.Pool.super_.prototype._destroy)
- description and source-code
```javascript
_destroy = function (client) {
  if (client._destroying) return
  client._destroying = true
  client.end()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Pool.super_.prototype._promise"></a>[function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>_promise (cb, executor)](#apidoc.element.pg.Pool.super_.prototype._promise)
- description and source-code
```javascript
_promise = function (cb, executor) {
  if (!cb) {
    return new this.Promise(executor)
  }

  function resolved (value) {
    process.nextTick(function () {
      cb(null, value)
    })
  }

  function rejected (error) {
    process.nextTick(function () {
      cb(error)
    })
  }

  executor(resolved, rejected)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Pool.super_.prototype._promiseNoCallback"></a>[function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>_promiseNoCallback (callback, executor)](#apidoc.element.pg.Pool.super_.prototype._promiseNoCallback)
- description and source-code
```javascript
_promiseNoCallback = function (callback, executor) {
  return callback
    ? executor()
    : new this.Promise(executor)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Pool.super_.prototype.connect"></a>[function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>connect (cb)](#apidoc.element.pg.Pool.super_.prototype.connect)
- description and source-code
```javascript
connect = function (cb) {
  return this._promiseNoCallback(cb, function (resolve, reject) {
    this.log('acquire client begin')
    this.pool.acquire(function (err, client) {
      if (err) {
        this.log('acquire client. error:', err)
        if (cb) {
          cb(err, null, function () {})
        } else {
          reject(err)
        }
        return
      }

      this.log('acquire client')
      this.emit('acquire', client)

      client.release = function (err) {
        delete client.release
        if (err) {
          this.log('destroy client. error:', err)
          this.pool.destroy(client)
        } else {
          this.log('release client')
          this.pool.release(client)
        }
      }.bind(this)

      if (cb) {
        cb(null, client, client.release)
      } else {
        resolve(client)
      }
    }.bind(this))
  }.bind(this))
}
```
- example usage
```shell
...

// instantiate a new client
// the client will read connection information from
// the same environment variables used by postgres cli tools
var client = new pg.Client();

// connect to our database
client.connect(function (err) {
  if (err) throw err;

  // execute a query on our database
  client.query('SELECT $1::text as name', ['brianc'], function (err, result) {
if (err) throw err;

// just print the result to the console
...
```

#### <a name="apidoc.element.pg.Pool.super_.prototype.end"></a>[function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>end (cb)](#apidoc.element.pg.Pool.super_.prototype.end)
- description and source-code
```javascript
end = function (cb) {
  this.log('draining pool')
  return this._promise(cb, function (resolve, reject) {
    this.pool.drain(function () {
      this.log('pool drained, calling destroy all now')
      this.pool.destroyAllNow(resolve)
    }.bind(this))
  }.bind(this))
}
```
- example usage
```shell
...
  client.query('SELECT $1::text as name', ['brianc'], function (err, result) {
    if (err) throw err;

    // just print the result to the console
    console.log(result.rows[0]); // outputs: { name: 'brianc' }

    // disconnect the client
    client.end(function (err) {
      if (err) throw err;
    });
  });
});

'''
...
```

#### <a name="apidoc.element.pg.Pool.super_.prototype.query"></a>[function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>query (text, values, cb)](#apidoc.element.pg.Pool.super_.prototype.query)
- description and source-code
```javascript
query = function (text, values, cb) {
  if (typeof values === 'function') {
    cb = values
    values = undefined
  }

  return this._promise(cb, function (resolve, reject) {
    this.connect(function (err, client, done) {
      if (err) {
        return reject(err)
      }
      client.query(text, values, function (err, res) {
        done(err)
        err ? reject(err) : resolve(res)
      })
    })
  }.bind(this))
}
```
- example usage
```shell
...
var client = new pg.Client();

// connect to our database
client.connect(function (err) {
  if (err) throw err;

  // execute a query on our database
  client.query('SELECT $1::text as name', ['brianc'], function (err, result) {
if (err) throw err;

// just print the result to the console
console.log(result.rows[0]); // outputs: { name: 'brianc' }

// disconnect the client
client.end(function (err) {
...
```

#### <a name="apidoc.element.pg.Pool.super_.prototype.take"></a>[function <span class="apidocSignatureSpan">pg.Pool.super_.prototype.</span>take (cb)](#apidoc.element.pg.Pool.super_.prototype.take)
- description and source-code
```javascript
take = function (cb) {
  return this._promiseNoCallback(cb, function (resolve, reject) {
    this.log('acquire client begin')
    this.pool.acquire(function (err, client) {
      if (err) {
        this.log('acquire client. error:', err)
        if (cb) {
          cb(err, null, function () {})
        } else {
          reject(err)
        }
        return
      }

      this.log('acquire client')
      this.emit('acquire', client)

      client.release = function (err) {
        delete client.release
        if (err) {
          this.log('destroy client. error:', err)
          this.pool.destroy(client)
        } else {
          this.log('release client')
          this.pool.release(client)
        }
      }.bind(this)

      if (cb) {
        cb(null, client, client.release)
      } else {
        resolve(client)
      }
    }.bind(this))
  }.bind(this))
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.Query"></a>[module pg.Query](#apidoc.module.pg.Query)

#### <a name="apidoc.element.pg.Query.Query"></a>[function <span class="apidocSignatureSpan">pg.</span>Query (config, values, callback)](#apidoc.element.pg.Query.Query)
- description and source-code
```javascript
Query = function (config, values, callback) {
  // use of "new" optional
  if(!(this instanceof Query)) { return new Query(config, values, callback); }

  config = utils.normalizeQueryConfig(config, values, callback);

  this.text = config.text;
  this.values = config.values;
  this.rows = config.rows;
  this.types = config.types;
  this.name = config.name;
  this.binary = config.binary;
  this.stream = config.stream;
  //use unique portal name each time
  this.portal = config.portal || "";
  this.callback = config.callback;
  if(process.domain && config.callback) {
    this.callback = process.domain.bind(config.callback);
  }
  this._result = new Result(config.rowMode, config.types);
  this.isPreparedStatement = false;
  this._canceledDueToError = false;
  this._promise = null;
  EventEmitter.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.super_"></a>[function <span class="apidocSignatureSpan">pg.Query.</span>super_ ()](#apidoc.element.pg.Query.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.Query.prototype"></a>[module pg.Query.prototype](#apidoc.module.pg.Query.prototype)

#### <a name="apidoc.element.pg.Query.prototype._getRows"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>_getRows (connection, rows)](#apidoc.element.pg.Query.prototype._getRows)
- description and source-code
```javascript
_getRows = function (connection, rows) {
  connection.execute({
    portal: this.portalName,
    rows: rows
  }, true);
  connection.flush();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.catch"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>catch (callback)](#apidoc.element.pg.Query.prototype.catch)
- description and source-code
```javascript
catch = function (callback) {
  return this.promise().catch(callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.handleCommandComplete"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleCommandComplete (msg, con)](#apidoc.element.pg.Query.prototype.handleCommandComplete)
- description and source-code
```javascript
handleCommandComplete = function (msg, con) {
  this._result.addCommandComplete(msg);
  //need to sync after each command complete of a prepared statement
  if(this.isPreparedStatement) {
    con.sync();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.handleCopyData"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleCopyData (msg, connection)](#apidoc.element.pg.Query.prototype.handleCopyData)
- description and source-code
```javascript
handleCopyData = function (msg, connection) {
  var chunk = msg.chunk;
  if(this.stream) {
    this.stream.handleChunk(chunk);
  }
  //if there are no stream (for example when copy to query was sent by
  //query method instead of copyTo) error will be handled
  //on copyOutResponse event, so silently ignore this error here
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.handleCopyInResponse"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleCopyInResponse (connection)](#apidoc.element.pg.Query.prototype.handleCopyInResponse)
- description and source-code
```javascript
handleCopyInResponse = function (connection) {
  if(this.stream) this.stream.startStreamingToConnection(connection);
  else connection.sendCopyFail('No source stream defined');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.handleDataRow"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleDataRow (msg)](#apidoc.element.pg.Query.prototype.handleDataRow)
- description and source-code
```javascript
handleDataRow = function (msg) {
  var row;

  if (this._canceledDueToError) {
    return;
  }

  try {
    row = this._result.parseRow(msg.fields);
  } catch (err) {
    this._canceledDueToError = err;
    return;
  }

  this.emit('row', row, this._result);
  if (this._accumulateRows) {
    this._result.addRow(row);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.handleEmptyQuery"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleEmptyQuery (con)](#apidoc.element.pg.Query.prototype.handleEmptyQuery)
- description and source-code
```javascript
handleEmptyQuery = function (con) {
  if (this.isPreparedStatement) {
    con.sync();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.handleError"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleError (err, connection)](#apidoc.element.pg.Query.prototype.handleError)
- description and source-code
```javascript
handleError = function (err, connection) {
  //need to sync after error during a prepared statement
  if(this.isPreparedStatement) {
    connection.sync();
  }
  if(this._canceledDueToError) {
    err = this._canceledDueToError;
    this._canceledDueToError = false;
  }
  //if callback supplied do not emit error event as uncaught error
  //events will bubble up to node process
  if(this.callback) {
    return this.callback(err);
  }
  this.emit('error', err);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.handlePortalSuspended"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handlePortalSuspended (connection)](#apidoc.element.pg.Query.prototype.handlePortalSuspended)
- description and source-code
```javascript
handlePortalSuspended = function (connection) {
  this._getRows(connection, this.rows);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.handleReadyForQuery"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleReadyForQuery (con)](#apidoc.element.pg.Query.prototype.handleReadyForQuery)
- description and source-code
```javascript
handleReadyForQuery = function (con) {
  if(this._canceledDueToError) {
    return this.handleError(this._canceledDueToError, con);
  }
  if(this.callback) {
    this.callback(null, this._result);
  }
  this.emit('end', this._result);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.handleRowDescription"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>handleRowDescription (msg)](#apidoc.element.pg.Query.prototype.handleRowDescription)
- description and source-code
```javascript
handleRowDescription = function (msg) {
  this._result.addFields(msg.fields);
  this._accumulateRows = this.callback || !this.listeners('row').length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.hasBeenParsed"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>hasBeenParsed (connection)](#apidoc.element.pg.Query.prototype.hasBeenParsed)
- description and source-code
```javascript
hasBeenParsed = function (connection) {
  return this.name && connection.parsedStatements[this.name];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.prepare"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>prepare (connection)](#apidoc.element.pg.Query.prototype.prepare)
- description and source-code
```javascript
prepare = function (connection) {
  var self = this;
  //prepared statements need sync to be called after each command
  //complete or when an error is encountered
  this.isPreparedStatement = true;
  //TODO refactor this poor encapsulation
  if(!this.hasBeenParsed(connection)) {
    connection.parse({
      text: self.text,
      name: self.name,
      types: self.types
    }, true);
  }

  if(self.values) {
    self.values = self.values.map(utils.prepareValue);
  }

  //http://developer.postgresql.org/pgdocs/postgres/protocol-flow.html#PROTOCOL-FLOW-EXT-QUERY
  connection.bind({
    portal: self.portalName,
    statement: self.name,
    values: self.values,
    binary: self.binary
  }, true);

  connection.describe({
    type: 'P',
    name: self.portalName || ""
  }, true);

  this._getRows(connection, this.rows);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.promise"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>promise ()](#apidoc.element.pg.Query.prototype.promise)
- description and source-code
```javascript
promise = function () {
  if (this._promise) return this._promise;
  this._promise = new Promise(function(resolve, reject) {
    this.once('end', resolve);
    this.once('error', reject);
  }.bind(this));
  return this._promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.requiresPreparation"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>requiresPreparation ()](#apidoc.element.pg.Query.prototype.requiresPreparation)
- description and source-code
```javascript
requiresPreparation = function () {
  //named queries must always be prepared
  if(this.name) { return true; }
  //always prepare if there are max number of rows expected per
  //portal execution
  if(this.rows) { return true; }
  //don't prepare empty text queries
  if(!this.text) { return false; }
  //prepare if there are values
  if(!this.values) { return false; }
  return this.values.length > 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.submit"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>submit (connection)](#apidoc.element.pg.Query.prototype.submit)
- description and source-code
```javascript
submit = function (connection) {
  if(this.requiresPreparation()) {
    this.prepare(connection);
  } else {
    connection.query(this.text);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.Query.prototype.then"></a>[function <span class="apidocSignatureSpan">pg.Query.prototype.</span>then (onSuccess, onFailure)](#apidoc.element.pg.Query.prototype.then)
- description and source-code
```javascript
then = function (onSuccess, onFailure) {
  return this.promise().then(onSuccess, onFailure);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.connection_parameters"></a>[module pg.connection_parameters](#apidoc.module.pg.connection_parameters)

#### <a name="apidoc.element.pg.connection_parameters.connection_parameters"></a>[function <span class="apidocSignatureSpan">pg.</span>connection_parameters (config)](#apidoc.element.pg.connection_parameters.connection_parameters)
- description and source-code
```javascript
connection_parameters = function (config) {
  //if a string is passed, it is a raw connection string so we parse it into a config
  config = typeof config == 'string' ? parse(config) : (config || {});
  //if the config has a connectionString defined, parse IT into the config we use
  //this will override other default values with what is stored in connectionString
  if(config.connectionString) {
    config = parse(config.connectionString);
  }
  this.user = val('user', config);
  this.database = val('database', config);
  this.port = parseInt(val('port', config), 10);
  this.host = val('host', config);
  this.password = val('password', config);
  this.binary = val('binary', config);
  this.ssl = typeof config.ssl === 'undefined' ? useSsl() : config.ssl;
  this.client_encoding = val("client_encoding", config);
  //a domain socket begins with '/'
  this.isDomainSocket = (!(this.host||'').indexOf('/'));

  this.application_name = val('application_name', config, 'PGAPPNAME');
  this.fallback_application_name = val('fallback_application_name', config, false);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.connection_parameters.prototype"></a>[module pg.connection_parameters.prototype](#apidoc.module.pg.connection_parameters.prototype)

#### <a name="apidoc.element.pg.connection_parameters.prototype.getLibpqConnectionString"></a>[function <span class="apidocSignatureSpan">pg.connection_parameters.prototype.</span>getLibpqConnectionString (cb)](#apidoc.element.pg.connection_parameters.prototype.getLibpqConnectionString)
- description and source-code
```javascript
getLibpqConnectionString = function (cb) {
  var params = [];
  add(params, this, 'user');
  add(params, this, 'password');
  add(params, this, 'port');
  add(params, this, 'application_name');
  add(params, this, 'fallback_application_name');

  if(this.database) {
    params.push("dbname='" + this.database + "'");
  }
  if(this.host) {
    params.push("host=" + this.host);
  }
  if(this.isDomainSocket) {
    return cb(null, params.join(' '));
  }
  if(this.client_encoding) {
    params.push("client_encoding='" + this.client_encoding + "'");
  }
  dns.lookup(this.host, function(err, address) {
    if(err) return cb(err, null);
    params.push("hostaddr=" + address);
    return cb(null, params.join(' '));
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.result"></a>[module pg.result](#apidoc.module.pg.result)

#### <a name="apidoc.element.pg.result.result"></a>[function <span class="apidocSignatureSpan">pg.</span>result (rowMode)](#apidoc.element.pg.result.result)
- description and source-code
```javascript
result = function (rowMode) {
  this.command = null;
  this.rowCount = null;
  this.oid = null;
  this.rows = [];
  this.fields = [];
  this._parsers = [];
  this.RowCtor = null;
  this.rowAsArray = rowMode == "array";
  if(this.rowAsArray) {
    this.parseRow = this._parseRowAsArray;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.result.prototype"></a>[module pg.result.prototype](#apidoc.module.pg.result.prototype)

#### <a name="apidoc.element.pg.result.prototype._getTypeParser"></a>[function <span class="apidocSignatureSpan">pg.result.prototype.</span>_getTypeParser (oid, format)](#apidoc.element.pg.result.prototype._getTypeParser)
- description and source-code
```javascript
function getTypeParser(oid, format) {
  format = format || 'text';
  if (!typeParsers[format]) {
    return noParse;
  }
  return typeParsers[format][oid] || noParse;
}
```
- example usage
```shell
...
  this.fields = [];
  this._parsers = [];
}
var ctorBody = "";
for(var i = 0; i < fieldDescriptions.length; i++) {
  var desc = fieldDescriptions[i];
  this.fields.push(desc);
  var parser = this._getTypeParser(desc.dataTypeID, desc.format || 'text');
  this._parsers.push(parser);
  //this is some craziness to compile the row result parsing
  //results in ~60% speedup on large query result sets
  ctorBody += inlineParser(desc.name, i);
}
if(!this.rowAsArray) {
  this.RowCtor = Function("parsers", "rowData", ctorBody);
...
```

#### <a name="apidoc.element.pg.result.prototype._parseRowAsArray"></a>[function <span class="apidocSignatureSpan">pg.result.prototype.</span>_parseRowAsArray (rowData)](#apidoc.element.pg.result.prototype._parseRowAsArray)
- description and source-code
```javascript
_parseRowAsArray = function (rowData) {
  var row = [];
  for(var i = 0, len = rowData.length; i < len; i++) {
    var rawValue = rowData[i];
    if(rawValue !== null) {
      row.push(this._parsers[i](rawValue));
    } else {
      row.push(null);
    }
  }
  return row;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.result.prototype.addCommandComplete"></a>[function <span class="apidocSignatureSpan">pg.result.prototype.</span>addCommandComplete (msg)](#apidoc.element.pg.result.prototype.addCommandComplete)
- description and source-code
```javascript
addCommandComplete = function (msg) {
  var match;
  if(msg.text) {
    //pure javascript
    match = matchRegexp.exec(msg.text);
  } else {
    //native bindings
    match = matchRegexp.exec(msg.command);
  }
  if(match) {
    this.command = match[1];
    //match 3 will only be existing on insert commands
    if(match[3]) {
      //msg.value is from native bindings
      this.rowCount = parseInt(match[3] || msg.value, 10);
      this.oid = parseInt(match[2], 10);
    } else {
      this.rowCount = parseInt(match[2], 10);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.result.prototype.addFields"></a>[function <span class="apidocSignatureSpan">pg.result.prototype.</span>addFields (fieldDescriptions)](#apidoc.element.pg.result.prototype.addFields)
- description and source-code
```javascript
addFields = function (fieldDescriptions) {
  //clears field definitions
  //multiple query statements in 1 action can result in multiple sets
  //of rowDescriptions...eg: 'select NOW(); select 1::int;'
  //you need to reset the fields
  if(this.fields.length) {
    this.fields = [];
    this._parsers = [];
  }
  var ctorBody = "";
  for(var i = 0; i < fieldDescriptions.length; i++) {
    var desc = fieldDescriptions[i];
    this.fields.push(desc);
    var parser = this._getTypeParser(desc.dataTypeID, desc.format || 'text');
    this._parsers.push(parser);
    //this is some craziness to compile the row result parsing
    //results in ~60% speedup on large query result sets
    ctorBody += inlineParser(desc.name, i);
  }
  if(!this.rowAsArray) {
    this.RowCtor = Function("parsers", "rowData", ctorBody);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.result.prototype.addRow"></a>[function <span class="apidocSignatureSpan">pg.result.prototype.</span>addRow (row)](#apidoc.element.pg.result.prototype.addRow)
- description and source-code
```javascript
addRow = function (row) {
  this.rows.push(row);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.result.prototype.parseRow"></a>[function <span class="apidocSignatureSpan">pg.result.prototype.</span>parseRow (rowData)](#apidoc.element.pg.result.prototype.parseRow)
- description and source-code
```javascript
parseRow = function (rowData) {
  return new this.RowCtor(this._parsers, rowData);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.type_overrides"></a>[module pg.type_overrides](#apidoc.module.pg.type_overrides)

#### <a name="apidoc.element.pg.type_overrides.type_overrides"></a>[function <span class="apidocSignatureSpan">pg.</span>type_overrides (userTypes)](#apidoc.element.pg.type_overrides.type_overrides)
- description and source-code
```javascript
function TypeOverrides(userTypes) {
  this._types = userTypes || types;
  this.text = {};
  this.binary = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.type_overrides.prototype"></a>[module pg.type_overrides.prototype](#apidoc.module.pg.type_overrides.prototype)

#### <a name="apidoc.element.pg.type_overrides.prototype.getOverrides"></a>[function <span class="apidocSignatureSpan">pg.type_overrides.prototype.</span>getOverrides (format)](#apidoc.element.pg.type_overrides.prototype.getOverrides)
- description and source-code
```javascript
getOverrides = function (format) {
  switch(format) {
    case 'text': return this.text;
    case 'binary': return this.binary;
    default: return {};
  }
}
```
- example usage
```shell
...
};

TypeOverrides.prototype.setTypeParser = function(oid, format, parseFn) {
  if(typeof format == 'function') {
    parseFn = format;
    format = 'text';
  }
  this.getOverrides(format)[oid] = parseFn;
};

TypeOverrides.prototype.getTypeParser = function(oid, format) {
  format = format || 'text';
  return this.getOverrides(format)[oid] || this._types.getTypeParser(oid, format);
};
...
```

#### <a name="apidoc.element.pg.type_overrides.prototype.getTypeParser"></a>[function <span class="apidocSignatureSpan">pg.type_overrides.prototype.</span>getTypeParser (oid, format)](#apidoc.element.pg.type_overrides.prototype.getTypeParser)
- description and source-code
```javascript
getTypeParser = function (oid, format) {
  format = format || 'text';
  return this.getOverrides(format)[oid] || this._types.getTypeParser(oid, format);
}
```
- example usage
```shell
...
  fallback_application_name: undefined,

  parseInputDatesAsUTC: false
};

var pgTypes = require('pg-types');
// save default parsers
var parseBigInteger = pgTypes.getTypeParser(20, 'text');
var parseBigIntegerArray = pgTypes.getTypeParser(1016, 'text');

//parse int8 so you can get your count values as actual numbers
module.exports.__defineSetter__("parseInt8", function(val) {
  pgTypes.setTypeParser(20, 'text', val ? pgTypes.getTypeParser(23, 'text') : parseBigInteger);
  pgTypes.setTypeParser(1016, 'text', val ? pgTypes.getTypeParser(1007, 'text') : parseBigIntegerArray);
});
...
```

#### <a name="apidoc.element.pg.type_overrides.prototype.setTypeParser"></a>[function <span class="apidocSignatureSpan">pg.type_overrides.prototype.</span>setTypeParser (oid, format, parseFn)](#apidoc.element.pg.type_overrides.prototype.setTypeParser)
- description and source-code
```javascript
setTypeParser = function (oid, format, parseFn) {
  if(typeof format == 'function') {
    parseFn = format;
    format = 'text';
  }
  this.getOverrides(format)[oid] = parseFn;
}
```
- example usage
```shell
...
var pgTypes = require('pg-types');
// save default parsers
var parseBigInteger = pgTypes.getTypeParser(20, 'text');
var parseBigIntegerArray = pgTypes.getTypeParser(1016, 'text');

//parse int8 so you can get your count values as actual numbers
module.exports.__defineSetter__("parseInt8", function(val) {
  pgTypes.setTypeParser(20, 'text', val ? pgTypes.getTypeParser(23, 'text') : parseBigInteger);
  pgTypes.setTypeParser(1016, 'text', val ? pgTypes.getTypeParser(1007, 'text') : parseBigIntegerArray);
});
...
```



# <a name="apidoc.module.pg.types"></a>[module pg.types](#apidoc.module.pg.types)

#### <a name="apidoc.element.pg.types.getTypeParser"></a>[function <span class="apidocSignatureSpan">pg.types.</span>getTypeParser (oid, format)](#apidoc.element.pg.types.getTypeParser)
- description and source-code
```javascript
function getTypeParser(oid, format) {
  format = format || 'text';
  if (!typeParsers[format]) {
    return noParse;
  }
  return typeParsers[format][oid] || noParse;
}
```
- example usage
```shell
...
  fallback_application_name: undefined,

  parseInputDatesAsUTC: false
};

var pgTypes = require('pg-types');
// save default parsers
var parseBigInteger = pgTypes.getTypeParser(20, 'text');
var parseBigIntegerArray = pgTypes.getTypeParser(1016, 'text');

//parse int8 so you can get your count values as actual numbers
module.exports.__defineSetter__("parseInt8", function(val) {
  pgTypes.setTypeParser(20, 'text', val ? pgTypes.getTypeParser(23, 'text') : parseBigInteger);
  pgTypes.setTypeParser(1016, 'text', val ? pgTypes.getTypeParser(1007, 'text') : parseBigIntegerArray);
});
...
```

#### <a name="apidoc.element.pg.types.setTypeParser"></a>[function <span class="apidocSignatureSpan">pg.types.</span>setTypeParser (oid, format, parseFn)](#apidoc.element.pg.types.setTypeParser)
- description and source-code
```javascript
function setTypeParser(oid, format, parseFn) {
  if(typeof format == 'function') {
    parseFn = format;
    format = 'text';
  }
  typeParsers[format][oid] = parseFn;
}
```
- example usage
```shell
...
var pgTypes = require('pg-types');
// save default parsers
var parseBigInteger = pgTypes.getTypeParser(20, 'text');
var parseBigIntegerArray = pgTypes.getTypeParser(1016, 'text');

//parse int8 so you can get your count values as actual numbers
module.exports.__defineSetter__("parseInt8", function(val) {
  pgTypes.setTypeParser(20, 'text', val ? pgTypes.getTypeParser(23, 'text') : parseBigInteger);
  pgTypes.setTypeParser(1016, 'text', val ? pgTypes.getTypeParser(1007, 'text') : parseBigIntegerArray);
});
...
```



# <a name="apidoc.module.pg.types.arrayParser"></a>[module pg.types.arrayParser](#apidoc.module.pg.types.arrayParser)

#### <a name="apidoc.element.pg.types.arrayParser.create"></a>[function <span class="apidocSignatureSpan">pg.types.arrayParser.</span>create (source, transform)](#apidoc.element.pg.types.arrayParser.create)
- description and source-code
```javascript
create = function (source, transform) {
  return {
    parse: function() {
      return array.parse(source, transform);
    }
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pg.utils"></a>[module pg.utils](#apidoc.module.pg.utils)

#### <a name="apidoc.element.pg.utils.normalizeQueryConfig"></a>[function <span class="apidocSignatureSpan">pg.utils.</span>normalizeQueryConfig (config, values, callback)](#apidoc.element.pg.utils.normalizeQueryConfig)
- description and source-code
```javascript
function normalizeQueryConfig(config, values, callback) {
  //can take in strings or config objects
  config = (typeof(config) == 'string') ? { text: config } : config;
  if(values) {
    if(typeof values === 'function') {
      config.callback = values;
    } else {
      config.values = values;
    }
  }
  if(callback) {
    config.callback = callback;
  }
  return config;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pg.utils.prepareValue"></a>[function <span class="apidocSignatureSpan">pg.utils.</span>prepareValue (value)](#apidoc.element.pg.utils.prepareValue)
- description and source-code
```javascript
function prepareValueWrapper(value) {
  //this ensures that extra arguments do not get passed into prepareValue
  //by accident, eg: from calling values.map(utils.prepareValue)
  return prepareValue(value);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
