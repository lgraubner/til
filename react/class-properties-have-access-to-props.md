# Class properties have access to props

When code is transpiled using Babel in combination with the stage-2 preset (as of writing) class properties are available on classes. This can be used to declare the initial state of a component. This reduces clutter and repeated typing of `super()`. The class properties have access to `this` (the class instance) and therefore access to props passed to the component.

```javascript
class MyComponent {
    state = {
        animal: this.props.animal
    }

    ...
}
```

## Sources

- [https://michalzalecki.com/react-components-and-class-properties/](https://michalzalecki.com/react-components-and-class-properties/)