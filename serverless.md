# serverless

`yarn local:api`

```js
"scripts": {
	"local:api": "./node_modules/.bin/sls offline -s stage"
}
```

serverless.js (backend) 與 signerUrl.js(frontend) `port` 要相同

serverless.js

```js
  custom: {
    "serverless-offline": {
      port: 3001
    },
```


src\constants\signerUrl.js

```js
const getSignerUrl = () => 
: "http://localhost:3001/";
```


```bash
Serverless: Starting Offline: stage/us-east-1.

Serverless: Routes for server:
Serverless: ANY /{proxy*}

Serverless: Offline listening on http://localhost:3001

Serverless: ANY /api/request_disclosure (λ: server)
```