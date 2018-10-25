# UWS library source
-------------------

## Why

- port of UWS from C++ for [DEPRECATED](https://www.reddit.com/r/node/comments/91kgte/uws_has_been_deprecated) nodejs build

## Usage
`uws` tries to mimic `ws` as closely as possible without sacrificing too much performance. In most cases you simply swap `require('ws')` with `require('uws')`:

```javascript

  npm install --save git+https://github.com/prod-alex-alex2006hw/uws.git

  var WebSocketServer = require('uws').Server;
  var wss = new WebSocketServer({ port: 3000 });

  function onMessage(message) {
      console.log('received: ' + message);
  }

  wss.on('connection', function(ws) {
      ws.on('message', onMessage);
      ws.send('something');
  });

```
