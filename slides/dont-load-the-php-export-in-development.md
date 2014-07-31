### Prevent the PHP export from loading in development

```php
// In functions.php
if ( ! defined( 'ACF_USE_LOCAL_CONFIGURATION' ) || ACF_USE_LOCAL_CONFIGURATION ) {
  require_once dirname( __FILE__ ) . '/advanced-custom-field-export.php';
}

// In your development wp-config.php
define('ACF_USE_LOCAL_CONFIGURATION', true);
```