---
title: node-mktmpio
---
#node-mktmpio

A simple Node.js module that includes a basic version of our CLI as an example.

<dl>
  <dt>GitHub</dt>
  <dd><a href="https://github.com/mktmpio/node-mktmpio">mktmpio/node-mktmpio</a></dd>
  <dt>npm</dt>
  <dd><a href="https://www.npmjs.com/package/mktmpio">mktmpio</a></dd>
</dl>

```js
var mktmpio = require('mktmpio');

mktmpio.create('redis', function(err, res) {
  if (err || res.error) {
    console.error('error creating instance:', err || res.error);
    return process.exit(1);
  }

  // Do stuff here:
  // res.host
  // res.port
  // res.password

  mktmpio.destroy(res.id, function(err, res) {
    if (err || res.error) {
      console.error('error terminating service:', err || res.error);
    } else {
      console.log('instance %s terminated', instance.id);
    }
  });
});
```
