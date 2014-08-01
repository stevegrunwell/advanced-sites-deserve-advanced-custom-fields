### Save your bacon!

```php
function themename_get_custom_field( $key, $id = null, $default = '' ) {
  global $post;
  $result = '';

  if ( function_exists( 'get_field' ) ) {
    if ( isset( $post->ID ) && ! $id ) {
      $result = get_field( $key );
    } else {
      $result = get_field( $key, $id );
    }

    if ( $result == '' ) {
      $result = $default;
    }
  } else { // get_field() is undefined
    $result = $default;
  }
  return $result;
}
```