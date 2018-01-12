# Dispatch exposes inner function

Dispatch return the inner function. Can be useful to wait for action to complete.

```javascript
const myAction = () => dispatch => {
    return dispatch(new Promise())
}

myAction.then(...)
```