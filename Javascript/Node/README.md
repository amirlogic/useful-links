# Node.js

Two realeases par year: In April and in October

Latest versions: 

20 (LTS)

22 (April 2024)


## Experimental Features (v22)

Env file ```node --env-file=.env app.js```

Execute scripts directly from the package.json

Ability to require ECMAScript modules (ESM) directly within CommonJS

Single Executable Applications (Bundle an app into a single executable)


## Recently Added Stable Native Features (v20)



Top level await

### Watch mode

```node --watch index.js```


### Native WebSocket client

```javascript
const socket = new WebSocket("ws://localhost:8080");
 
socket.addEventListener("open", (event) => {
  socket.send("Hello Server!");
});
 
socket.addEventListener("message", (event) => {
  console.log("Message from server ", event.data);
});
```


### Test runner

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


## Fetch API (since v18)

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
