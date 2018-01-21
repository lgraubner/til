# Static constant to resolve class name

PHP classes have a static constant which resolves to a fully qualified class name. This is useful for usage of classes in namespaced environments.

```php
<?php
namespace foo {
    class bar {
    }

    echo bar::class; // foo\bar
}
?>
```