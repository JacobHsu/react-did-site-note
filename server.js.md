# server.js

yarn add serverless-express uport-credentials did-jwt


serverless.js

```js
  plugins: [
    "serverless-express",
    "serverless-scriptable-plugin",
    "serverless-plugin-include-dependencies",
    "serverless-offline",
    "serverless-stack-output"
  ],
```

package.json

```js
"devDependencies": {
    "serverless-offline": "^4.9.4",
    "serverless-plugin-include-dependencies": "^3.2.1",
    "serverless-stack-output": "^0.2.3"
  },
"dependencies": {
	"serverless": "^1.41.0",
    "serverless-express": "^2.0.11",
    "serverless-scriptable-plugin": "^1.0.0",
```

`$ yarn add serverless-offline serverless-plugin-include-dependencies serverless-stack-output --dev`

`$ yarn add serverless serverless-express serverless-scriptable-plugin`

```js
"scripts": {
	"local:api": "./node_modules/.bin/sls offline -s stage"
}
```
> /.bin/sls  `yarn add serverless`


## ! FIXID

> serverless-offline 降版 `yarn lcaol:api` 才正常

`yarn add serverless@^1.41.0`
`yarn add serverless-offline@^4.9.4 --dev`   "serverless-offline": "^6.1.4",


offline: [HTTP] server ready: http://localhost:3000

```js
$ ./node_modules/.bin/sls offline -s stage
Serverless: Starting Offline: stage/us-east-1.

Serverless: Routes for server:
Serverless: ANY /{proxy*}

Serverless: Offline listening on http://localhost:3001
```
