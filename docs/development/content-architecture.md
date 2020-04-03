# Content architecture

The OpenEuropa project does not enforce a strict content architecture but provides corporate solutions used by the European Commission.

## Content types

The [OpenEuropa Content](https://github.com/openeuropa/oe_content) component provides a growing number of corporate content types intended to harmonize the content architecture across the sites of the European Commission. Moreover, it provides RDF-based support for the corporate vocabularies published by the [European Publication Office (OP)](https://publications.europa.eu/en/home).

Corporate content types result from content governance work at DG COMM and they should be approved by it, before any implementation work can start.


### Development guidelines for content types
When implementing corporate content types stick to the following guidelines:

- One dedicated submodule with content type configuration in oe_content.
- One dedicated submodule theming that content type in oe_theme.

#### oe_content submodule
A corporate content submodule should only have basic configuration and logic and basic data related dependencies:
- bundle definition;
- content type specific field storages and field instances;
- view modes.

Configuration shipped as content submodules is intended as initial configuration:
- After being installed and imported the content type belongs to the site.
- The submodule will not update existing configuration after install.

Content should be made translatable providing the related language configuration in the config/optional folder.

The following points should be followed on content types development:
- Check if existing fields could be reused before implementing a new one.
- Prefix corporate fields only with oe_ so to reduce the risk of naming conflict.
- Base fields are common to all bundles and should already be present in all content types, no need to implement in new ones.
- Prefer API validation, do not rely on Form API validation.
- Publication Office (PO) vocabularies are the only allowed taxonomies.
- If not yet imported, it can be added in the triple-store.
- Select the appropriated field types: 
- Core/contrib field types preferred.
  - New field types if required.
  - Compound fields as corporate content entities if required.

Any custom field type, entity validation, entity wrappers, etc. should be covered by PHPUnit tests.

The business requirements should be covered in a Behat test:
- available fields and their configuration (required, max length, etc.).
- referenceable content entities.

#### oe_theme submodule
All theming logic for the content type should be created in the appropriated oe_theme submodule.

A theming submodule provides:
- view mode display overrides in the config/overrides folder.
- display overrides will be installed once and replace any existing configuration.
- `PageHeaderMetadata` plugin if needed.
- templates specific to this content type rendering.
- any other configuration that is needed for this content type, properly namespaced (dates, image styles).

Test coverage should cover:
- any business related functionality on the frontend level, e.g.:
- changing of labels in the frontend based on a condition (field value, time, etc.)
- rendering of data in the expected way.
- access checks.
- caching.

Tests should be executed as anonymous user, using the existing entity creation and update steps to ensure cache invalidation, and with the correct user to ensure access checks.

## Page building

To support the building of pages with a variety of page-level elements, the [OpenEuropa Paragraphs](https://github.com/openeuropa/oe_paragraphs) component provides a number of Drupal paragraph types that can be used
on any content type. Combined with the [OpenEuropa Theme](https://github.com/openeuropa/oe_theme), these are displayed using the [Europa Component Library (ECL)](https://ec.europa.eu/component-library) style guide.