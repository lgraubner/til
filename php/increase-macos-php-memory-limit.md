# Increase MacOS PHP memory limit

Sometimes it's useful to increase the local PHP memory limit. For example a local `composer update` needs more memory than the default 128M.

```
# Find used php.ini
php -r 'phpinfo();' | grep 'php.ini'

# edit php.ini
sudo vim /path/to/php.ini # set memory_limit = -1 (unlimited)

# check if it worked
php -r "echo ini_get('memory_limit').PHP_EOL;"
```