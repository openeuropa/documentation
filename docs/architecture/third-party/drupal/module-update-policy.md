# Module update policy

Drupal modules are updated using the [update API for Drupal 8][1] by implementing the following hooks:

- [`hook_update_N`][2]
- [`hook_post_update_NAME`][3]

Since `hook_post_update_NAME` hooks are executed alphabetically we prepend `_NAME` with an incremental numeric string,
so that we can be sure they are executed in the right order.

Our current convention is a 5-digits numeric string starting from `00001`, as shown below:

```php
/**
 * A meaningful comment describing the first update.
 */
function MY_MODULE_post_update_00001() { ... }

/**
 * Another meaningful comment describing the second update.
 */
function MY_MODULE_post_update_00002() { ... }
```

We suggest not to append anything after the sequence number as doing so will eliminate the risk of having hooks with the same number. Instead, we suggest to add a meaningful comment on top of each hook, that will be displayed when running `drush updb`.

[1]: https://www.drupal.org/docs/8/api/update-api/introduction-to-update-api-for-drupal-8
[2]: https://api.drupal.org/api/drupal/core!lib!Drupal!Core!Extension!module.api.php/function/hook_update_N
[3]: https://api.drupal.org/api/drupal/core!lib!Drupal!Core!Extension!module.api.php/function/hook_post_update_NAME
