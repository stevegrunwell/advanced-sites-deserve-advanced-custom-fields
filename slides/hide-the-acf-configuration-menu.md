### Hide the ACF configuration menu

Simply drop the following in your wp-config.php file to prevent clients from creating (or editing) custom fields:

```php
define('ACF_LITE', true);
```