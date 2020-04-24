# API

[login with uport] qr-code

http://localhost:3001/api/request_disclosure

client
src\sagas\credentials.js

requestDisclosure(action) {

src\server.js

server.js
```js
app.post("/api/request_disclosure", async (req, res) => {
```


src\index.js

```js
import sagas from "./sagas";
const sagaMiddleware = createMiddleware();
const store = configureStore(rootReducer, sagaMiddleware, routerMiddleware(history));
sagaMiddleware.run(sagas);
```


sagas\credentials.js

```js
import { spawn, takeEvery, put, call } from "redux-saga/effects";
import { transport } from "uport-transports";
import { captureException } from "@sentry/browser";
```