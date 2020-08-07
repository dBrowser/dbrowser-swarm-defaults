# DatLand Swarm Defaults

DatLand Swarm Defaults gives you the DWeb defaults for [Discovery-Swarm](https://www.npmjs.com/package/dweb-discovery-swarm). This will set your *dns* and *dht* servers making it easy to discover other peers. 


## Usage 

Create a config object and pass it to discovery swarm. 

Any options you specify will overwrite the defaults. See discovery swarm for options.

```javascript
var Swarm = require('dweb-discovery-swarm')
var swarmDefaults = require('dbrowser-swarm-defaults')

// Create a DWebFs here

var config = swarmDefaults({
  stream: function () {
    return drive.createPeerStream()
  }
})
var swarm = Swarm(config)
```

[See a full DWeb example](https://gist.github.com/joehand/1e644adc3cc43ae05855)