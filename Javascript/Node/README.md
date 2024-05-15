# Node.js

Two realeases par year: In April and in October

Latest versions: 
20 (LTS)
22 (April 2024)


## Experimental Features

Execute scripts directly from the package.json

Ability to require ECMAScript modules (ESM) directly within CommonJS


## Latest native support

Env file

Top level await

Refresh

Native WebSocket client


### Stable test runner

```javascript
import { test, mock } from 'node:test';
import assert from 'node:assert';
import fs from 'node:fs';

mock.method(fs, 'readFile', async () => "Hello World");
test('synchronous passing test', async (t) => {
  // This test passes because it does not throw an exception.
  assert.strictEqual(await fs.readFile('a.txt'), "Hello World");
});
```


## Fetch API

```javascript

  // Default options are marked with *
  fetch(url, {
    method: "POST", // *GET, POST, PUT, DELETE, etc.
    mode: "cors", // no-cors, *cors, same-origin
    cache: "no-cache", // *default, no-cache, reload, force-cache, only-if-cached
    credentials: "same-origin", // include, *same-origin, omit
    headers: {
      "Content-Type": "application/json",
      // 'Content-Type': 'application/x-www-form-urlencoded',
    },
    redirect: "follow", // manual, *follow, error
    referrerPolicy: "no-referrer", // no-referrer, *no-referrer-when-downgrade, origin, origin-when-cross-origin, same-origin, strict-origin, strict-origin-when-cross-origin, unsafe-url
    body: JSON.stringify(data), // body data type must match "Content-Type" header
  })
.then((response)=>{
  console.log(response.json()) // parses JSON response into native JavaScript objects
})

```
