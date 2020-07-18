# Dat Swarm Defaults

[![npm][npm-image]][npm-url]
[![travis][travis-image]][travis-url]
[![standard][standard-image]][standard-url]

Use Dat defaults for `dns` and `dht` servers in [hyperdiscovery](https://github.com/datproject/hyperdiscovery) or [dweb-discovery-swarm](https://github.com/mafintosh/dweb-discovery-swarm). The *dns* and *dht* servers are used to discover other peers.

### Using Other Discovery Servers

Run discovery servers with [dns-discovery](https://github.com/mafintosh/dns-discovery#cli) or a [bittorrent-dht](https://github.com/webtorrent/bittorrent-dht) server (such as https://github.com/dwswarm/dht).

## Usage

Create a config object and pass it to discovery swarm.

Any options you specify will overwrite the defaults. See discovery swarm for options.

```javascript
var Swarm = require('dweb-discovery-swarm')
var defaults = require('dat-swarm-defaults')

var config = defaults({
  stream: function () {
    return drive.createPeerStream()
  }
})
var swarm = Swarm(config)
```

## License

[MIT](LICENSE.md)

[npm-image]: https://img.shields.io/npm/v/dat-swarm-defaults.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/dat-swarm-defaults
[travis-image]: https://img.shields.io/travis/datproject/dat-swarm-defaults.svg?style=flat-square
[travis-url]: https://travis-ci.org/datproject/dat-swarm-defaults
[standard-image]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square
[standard-url]: http://npm.im/standard

