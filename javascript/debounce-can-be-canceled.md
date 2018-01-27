# Debounce can be canceled

Lodash has a useful [debounce function](https://lodash.com/docs/4.17.4#debounce). This function waits a given duration until the given function is executed. This duration is resetted everytime the debounce function is called again and therefore debounces the execution. This is for example useful for scroll events where it might be useful to execute it right after the scrolling stopped.

This function also has a cancel function. This is good to have when using with React because debounced functions and unmounted components do not play well together.

```javascript
class MyComponent {
    componentWillUnmount() {
        this.handleClick.cancel()
    }

    handleClick = () => debounce({
        console.log('debounced click');
    }, 200)

    render() {
        return (
            <button onClick={this.handleClick}>Click Me</button>
        )
    }
}

```