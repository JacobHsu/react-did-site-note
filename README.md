# react-did-site-note


## reducers


selectors\index.js

```js
export const isLoading = state => Boolean(state.loading.length);
```

components\Registration\LandingContainer.js

```js
import {  isLoading } from "../../selectors";
import Landing from "./Landing";
const mapStateToProps = state => ({
  isLoading: isLoading(state),
});
export default connect(mapStateToProps, mapDispatchToProps)(Landing);
```

components\Registration\Landing.js

```js
export default withTranslation()(Landing);
```

src\index.js

```js
import createRootReducer from "./reducers";

const rootReducer = createRootReducer(history);
const store = configureStore(rootReducer, sagaMiddleware, routerMiddleware(history));

const render = Component => ReactDOM.render(
  <Provider store={store}>
    <Component />
  </Provider>
  ...
);
```

src\reducers\index.js

```js
import loading from "./loading";
function createRootReducer(history) {
  return combineReducers({
  	loading,
```
