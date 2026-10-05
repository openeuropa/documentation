# Forms

The Form API in Drupal follows an object oriented architecture, forms being defined as classes. With this come many of the OOP benefits such as [dependency injection](services-dependency-injection.md) and testability.

## Creating a form

Form classes need to implement `\Drupal\Core\Form\FormInterface` but typically extend `Drupal\Core\Form\FormBase`. As such there are a few methods that need to be implemented for processing of a form:

* A form has an ID -> the `getFormId()` method
* A form is defined as a multitude of form elements (render array) -> the `buildForm(array $form, FormStateInterface $form_state)` method
* A form can be validated before it is submitted -> the `validateForm(array &$form, FormStateInterface $form_state)` method
* A form is submitted using the `submitForm(array &$form, FormStateInterface $form_state)` method.

The *form state* is a `Drupal\Core\Form\FormStateInterface` object.

For an example of a simple form definition and the methods that can/need to be implemented in a form, check out [this page](https://www.drupal.org/docs/drupal-apis/form-api/introduction-to-form-api).

## Form elements

A form definition is a collection of form elements, defined as arrays. The Form API comes with a number of form elements by default. 

See here the [complete list](https://api.drupal.org/api/drupal/elements) of form elements provided by core. Look for the ones of the type `FormElement`.

Form elements (`FormElementInterface`) extend render elements (`ElementInterface`) and integrate with the [render system](https://www.drupal.org/docs/drupal-apis/render-api).

The best way to discover how to use a particular form element (or render element for that matter) is to inspect the class and its documentation. For example, the `textfield` form element is defined in `Drupal\Core\Render\Element\Textfield` and an example of how it's used can be found in the class documentation.

## Building and rendering a form

There are 2 main ways to build and render a form: from a route definition (form page) or programmatically.

### Route handler

Forms can be mapped to a route by using the `_form` key inside the `defaults` section of the route definition. See [this example](https://www.drupal.org/docs/drupal-apis/form-api/introduction-to-form-api#fapi-in-route) and read more about the [routing system](routing-system.md).

### Programmatically

Forms can also be retrieved and rendered from controllers and other places. The `Drupal\Core\Form\FormBuilder` service can be used for this (service key: `form_builder`). See an example [here](https://www.drupal.org/docs/drupal-apis/form-api/introduction-to-form-api#fapi-build-programatically).

## Altering forms

Forms can be altered using [hook_form_alter()](https://api.drupal.org/api/drupal/core%21lib%21Drupal%21Core%21Form%21form.api.php/function/hook_form_alter), [hook_form_FORM_ID_alter()](https://api.drupal.org/api/drupal/core%21lib%21Drupal%21Core%21Form%21form.api.php/function/hook_form_FORM_ID_alter) and [hook_form_BASE_FORM_ID_alter()](https://api.drupal.org/api/drupal/core%21lib%21Drupal%21Core%21Form%21form.api.php/function/hook_form_BASE_FORM_ID_alter). 

## Form bases

Typically, forms in Drupal extend `Drupal\Core\Form\FormBase`. However, there are a few other base classes that can be used depending on the purpose of the form:

* `Drupal\Core\Form\ConfigFormBase` -> provides defaults for interacting with the configuration API for storing config defined via the form 
  * see [here](https://www.drupal.org/docs/drupal-apis/form-api/configformbase-with-simple-configuration-api) an example on how to use this
  * see [here](https://www.drupal.org/docs/drupal-apis/configuration-api) more information about the Configuration API
* `Drupal\Core\Form\ConfirmFormBase` -> provides defaults for creating a confirmation form (see [here](https://www.drupal.org/docs/drupal-apis/form-api/confirmformbase-to-confirm-an-action) an example on how to use this)

