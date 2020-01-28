# Adding a sidebar to your subtheme

In order to add a sidebar to your subtheme you can do the following:

## Step 1: Add a region to your subtheme

Open up you `subtheme.info.yml` file and add `sidebar: "Sidebar"` to the regions section.

## Step 2: Override the block part of the page template

Create a file `subtheme/template/page.html.twig` and add the following contents:

```
{% extends "@oe_theme/layout/page.html.twig" %}

{% set _main_content_class = page.sidebar ? 'ecl-col-12 ecl-col-lg-9' : 'ecl-col' %}

{% block content %}
  <section class="main-content ecl-u-mv-l">
    <div class="ecl-container">
      <div class="ecl-row">
        {% if page.sidebar %}
          <div class="ecl-col-12 ecl-col-lg-3">
            {{ page.sidebar }}
          </div>
        {% endif %}
        <div class="{{ _main_content_class }}">
          {{ page.content }}
        </div>
      </div>
    </div>
  </section>
{% endblock %}
```

A quick explanation:

`extends` tells the template to work on top of that file, `@oe_theme` refers to the base theme you are extending.
`block content` will overwrite only that part of the extended template.


