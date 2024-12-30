# Javascript ressources


## Libraries

Zod: schema declaration and validation library https://zod.dev/

Async: powerful functions for working with asynchronous JavaScript https://caolan.github.io/async/v3/

Nano ID: unique string ID generator for JavaScript https://www.npmjs.com/package/nanoid

Date-fns (Lodash for Date): https://www.npmjs.com/package/date-fns

PDF.js https://mozilla.github.io/pdf.js/


## Rate Limit

Upstash Ratelimit https://www.npmjs.com/package/@upstash/ratelimit

Rate Limiter Flexible https://www.npmjs.com/package/rate-limiter-flexible


## Js New Methods

```structuredClone```  https://developer.mozilla.org/en-US/docs/Web/API/structuredClone


## Js API Frameworks

Hono (use in CloudFlare Workers) https://hono.dev


## Array.forEach vs Array.map

```forEach``` just executes a function for each element, can be used to modify the original array

```map``` returns another array


## CMD arguments

```javascript
import * as process from "node:process"

const filename = process.argv[2];
```

## Buffers

A buffer is a space in memory (typically RAM) that stores binary data. 

There are two ways of creating a buffer:

```const demoBuf = Buffer.alloc(1024);```

To create a buffer from pre-existing data, we use the from() method.

```const stringBuf = Buffer.from('This is a string');```

Note that it is possible to create a buffer from another buffer to copy the data.


### Buffer Methods

To get back the string from the buffer: ```stringBuf.toString();```

toString() takes an optional parameter which is encoding.

If we wanted to change the contents of the entire buffer, we can use the write() method. The write() method accepts a string that will replace the contents of a buffer.

To copy data from one buffer to the other, we’ll use the copy() method on the buffer that’s the source of the information.


## Base64

```javascript
const encodedData = btoa("Hello, world"); // encode a string
const decodedData = atob(encodedData); // decode the string
```


## Misc

Alternative to Js Objects https://www.youtube.com/watch?v=hRSwSAr-gok

Maps vs Objects https://www.youtube.com/watch?v=hubQQ3F337A

HTML Table from dataset https://tabulator.info

SQLite in the Browser https://sql.js.org

Hosting read-only SQLite databases on static file hosters https://github.com/phiresky/sql.js-httpvfs



