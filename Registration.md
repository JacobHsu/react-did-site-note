
# Registration


routes\index.js

```js
<Route path={registration.path} render={() =>
	<App serviceId={registration.serviceId}>
		<Registration />
	</App>} />	
```

components\Registration\index.js

```js
<Route path={SERVICES[serviceId].url} exact render={() =>
  <React.Fragment>
    <BackButton url="/" />
    <Landing />
  </React.Fragment>}
```


Registration\Landing.js

```js
 ? <LoginLink href={login.url} />
```