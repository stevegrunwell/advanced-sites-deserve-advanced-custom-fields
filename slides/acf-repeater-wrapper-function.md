#### ACF Repeater Wrapper Function

```php
function themename_get_repeater_content( $key, $id = null, $fields = array() ) {
  global $post;
  if ( ! $id ) $id = $post->ID;
  $values = array();

  if ( themename_get_custom_field( $key, $id, false ) &&
    function_exists( 'has_sub_field' ) &&
    function_exists( 'get_sub_field' ) ) {

    while ( has_sub_field( $key, $id ) ) {
      $value = array();
      foreach ( $fields as $field ){
        $value[ $field ] = get_sub_field( $field );
      }
      if( ! empty( $value ) ) {
        $values[] = $value;
      }
    }
  }
  return $values;
}
```