## Using Advanced Custom Fields

ACF has two functions, `the_field()` and `get_field()`, which print or retrieve the custom field, respectively.

* **$field_name** - The ACF field slug (e.g. hero_image)
* **$post_id** - The ID of the post to retrieve `$field_name` from
* **$format_output** - Apply ACF formatting to the output?