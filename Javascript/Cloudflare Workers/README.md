# Cloudflare Workers

The Cloudflare Workers runtime is built on top of the V8 JavaScript and WebAssembly engine. The Workers runtime is updated at least once a week, to at least the version of V8 that is currently used by Google Chrome's stable release. This means you can safely use the latest JavaScript features, with no need for transpilers.


## Getting started

https://www.youtube.com/watch?v=H7Qe96fqg1M

```bash
npm create cloudflare
```

Initializes the app and installs dependencies

```npx wrangler login```

Install wrangler: ```npx wrangler```

Cheking: ```npx wrangler whoami```

Deploying: ```npm run deploy```


## CF Specific Stuffs

### request object

Hello World

```javascript
export default {
	async fetch(request, env, ctx) {
		return new Response('Just playing with workers!');
	},
};
```

### Response

Can have a second parameter:

```javascript
Response('Just playing with workers!',
	{
		headers:{
			'Content-Type':'application/json'
		}
	})
```

### Configuration

Compatibility date


## Hono

A Javascript framework for http requests

```npm install hono```

Then we can put this in the source file:

```javascript

import { Hono } from 'hono'
const app = new Hono()

app.get('/', (c) => c.text('Hono!'))

export default app

```

### API

Query parameters: 

```javascript
app.get('/search', (c) => {
  const query = c.req.query('q')
  ...
})
```

All parameters at once:

```javascript
app.get('/search', (c) => {
  const { q, limit, offset } = c.req.query()
  ...
})
```

Method:

```javascript
app.get('/about/me', (c) => {
  const method = c.req.method // `GET`
  ...
})
```

