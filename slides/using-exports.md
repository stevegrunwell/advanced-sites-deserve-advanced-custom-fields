##  Using Exports

* Best to run client sites from the PHP export:
```php
# In your functions.php
require_once dirname( __FILE__ ) . '/advanced-custom-field-export.php';
```
* Always include the XML export in case you need to make changes later!