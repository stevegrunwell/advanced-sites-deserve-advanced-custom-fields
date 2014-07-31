### A sister function

You might also consider adding the following shortcut:

```php
function themename_custom_field( $key, $id = null, $default = '' ) {
  echo themename_get_custom_field( $key, $id, $default );
}
```