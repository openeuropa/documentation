# Module update policy

Drupal modules are updated using the [update API for Drupal 8][1] by implementing the following hooks:

- [`hook_update_N`][2]
- [`hook_post_update_NAME`][3]

Since `hook_post_update_NAME` hooks are executed alphabetically we have to prepend `_NAME` with the same numeric value
that we use on `hook_update_N`, meaning:

- First 1 or 2 digits for Drupal core compatibility (Drupal 8, 9, 10, etc.).
- Following 1 digit for your module's major release version; for example, `0.x` use `0`, `1.x` use `1`, for `2.x` use `2`, etc.
- Following 2 digits for sequential counting, starting with `01`. **Note that the `x000` number can never be used**: the lowest
update number that will be recognized and run for major version `x` is `x001`.

[1]: https://www.drupal.org/docs/8/api/update-api/introduction-to-update-api-for-drupal-8
[2]: https://api.drupal.org/api/drupal/core!lib!Drupal!Core!Extension!module.api.php/function/hook_update_N
[3]: https://api.drupal.org/api/drupal/core!lib!Drupal!Core!Extension!module.api.php/function/hook_post_update_NAME
