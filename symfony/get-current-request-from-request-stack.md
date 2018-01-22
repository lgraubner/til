# Get current request from request stack

Symfony provides a `RequestStack` service to get the last request from places the original `Request` object is not available such as event listeners.

```php
class Foo
{
    public function myFunc()
    {
        $requestStack = $this->get('request_stack');
        $request = $requestStack->getCurrentRequest();
    }
}
```