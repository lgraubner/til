# Services in controller actions

As of Symfony 3.3 everything is a service, even controllers. But instead of initializing services to use in the constructor they should be fetched in the corresponding controller action.

Bad:

```php

class ExampleController extends Controller
{
    public function __construct(Service $service)
    {
        $this->service = $service;
    }

    public function exampleAction(Request $request)
    {
        $this->service->method();
    }
}
```

Good:

```php
class ExampleControler extends Controller
{
    public function exampleAction(Request $request)
    {
        $service = $this->get('service');
        $service->method();
    }
}
```

Why? In the first example the service gets instantiated on every route even if it's not used.