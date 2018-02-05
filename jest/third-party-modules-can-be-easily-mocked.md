# Third party modules can be easily mocked

With Jest it's quite easy to mock third party modules.

```javascript
jest.mock('external-module', () => ({
    anFunction: jest.fn(() => 'return value')
}))
```