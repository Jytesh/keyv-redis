# keyv-redis

> Redis storage adapter for Keyv

[![Build Status](https://travis-ci.org/lukechilds/keyv-redis.svg?branch=master)](https://travis-ci.org/lukechilds/keyv-redis)
[![Coverage Status](https://coveralls.io/repos/github/lukechilds/keyv-redis/badge.svg?branch=master)](https://coveralls.io/github/lukechilds/keyv-redis?branch=master)
[![npm](https://img.shields.io/npm/v/keyv-redis.svg)](https://www.npmjs.com/package/keyv-redis)

## Install

```shell
npm install --save keyv-redis
```

## Usage

```js
const Keyv = require('keyv');
const KeyvRedis = require('keyv-redis');

const redis = new KeyvRedis('redis://user:secret@localhost:6379');
const keyv = new Keyv({ store: redis });
```

## API

### new KeyvRedis([options])

Returns a Keyv storage adapter for Redis.

#### options

Type: `undefined`, `string`, `object`<br>
Default: `undefined`

A Redis connection URI string or connection object. If `undefined`, default Redis settings will be used. View [`redis.createClient()`](https://github.com/NodeRedis/node_redis#rediscreateclient) docs for more info.

## License

MIT © Luke Childs
