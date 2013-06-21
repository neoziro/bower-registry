# bower-registry [![Build Status](https://travis-ci.org/neoziro/bower-registry.png?branch=master)](https://travis-ci.org/neoziro/bower-registry)

Simple bower registry using node and redis.

## How to use

### From command line

```
bower-registry -d redis
```

### In node

```javascript
var bowerRegistry = require('bower-registry'),
    Registry = bowerRegistry.Registry,
    RedisDb = bowerRegistry.RedisDb;

var registry = new Registry({
  db: new RedisDb()
});

registry
  .initialize()
  .listen(3000);
```

## Command line

```
  Usage: bower-registry [options]

  Options:

    -h, --help                output usage information
    -V, --version             output the version number
    -d, --database <value>    Database
    -o, --db-options [value]  Database options
    -p, --port <value>        Web server port
    -h, --host [value]        Web server host
    -P, --private             Accept private packages
```

## License

MIT