# OpenEuropa Showcase Page

This module is part of  [OpenEuropa Showcase profile](https://github.com/openeuropa/oe_showcase), it provides the content type OE Showcase Page which allows the creation of nodes with multiple content configuration using paragraph components.

## How to create or edit an OE Showcase Page:

In order to add oe edit an OE Showcase Page on your site, go to the Drupal Content Management page `admin/content` and locate the content you would like to edit or click on Add Content to create a new page.

## How to add paragraphs to a page:

The Paragraph[^1] types provided by the OpenEuropa Paragraphs[^2] :
- Accordion
- Accordion item
- Links block
- Listing item
- Listing Item Block
- Quote
- Rich text
- Text with Featured media
- Document

### Step 1 - Adding a paragraph:
In order to add paragraphs to a page, create a new page or edit an existing one.

1 - On the body field click on the dropdown arrow to reveal the available paragraphs types.

2 - Select the desired paragraph, e.g. Accordion and fill out the required fields (Title and Body).

3 - Scroll to the bottom of the form and click on Save to save and display the content.

### Step 2 - Reordering paragraphs

The order of each paragraph can also be rearranged  by dragging and dropping them using the move cursor icon to the left of each paragraph.

## Recommendation

- [OpenEuropa Showcase Navigation](https://github.com/openeuropa/oe_showcase): Together with OpenEuropa Showcase Default Content provides default configuration of menu links to each showcase page.
- [OpenEuropa Showcase Default Content](https://github.com/openeuropa/oe_showcase): Provides default demo content with several pages demonstrating the use of paragraphs. This module is based on the [Default Content](https://www.drupal.org/project/default_content) module, for further instructions on how to export/import content please refer to its page for updated information.

## Configuration

This module uses the [Configuration development](https://www.drupal.org/project/config_devel) to manage configuration.

To export configuration using drush type:
```
$ ./vendor/bin/drush cde oe_showcase_page
```

To import configuration using drush type:
```
$ ./vendor/bin/drush cdi oe_showcase_page
```

[^1]: For in-depth information on the Paragraphs module, visit the project page: https://www.drupal.org/project/paragraphs

[^2]: For in-depth information on the OpenEuropa Paragraphs module, visit the GitHub page: https://github.com/openeuropa/oe_paragraphs
