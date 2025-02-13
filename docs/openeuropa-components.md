# OpenEuropa components

Below the list of loosely coupled, reusable PHP projects provided by the OpenEuropa Initiative.
Each project complies with [PHP-FIG][1] standards and adhere to the best-practices put forward by [PHP The "Right" Way][2].

Most code is distributed on [Packagist][3] and released under the [EUPL-1.2 license][4].

All projects use Semantic Versioning. Attention is drawn to [item 4 of the Semantic Version specification](https://semver.org/#spec-item-4)
'Major version zero (0.y.z) is for initial development. Anything may change at any time. The public API should not be considered stable.'

### Drupal projects

<table>
    <tr>
        <th>Component</th>
        <th>Status</th>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_authentication"><b>OpenEuropa Authentication</b></a><br/>
        This module allows to authenticate users against the European Commission login service. Details of this service can be found <a href="https://webgate.ec.europa.eu/cas/about.html">here</a>.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_authentication"><img src="https://img.shields.io/packagist/v/openeuropa/oe_authentication.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_authentication"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_authentication/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_authentication"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_authentication.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_content"><b>OpenEuropa Content</b></a><br/>
    This component ships with corporate and standardised content and entity types, as well as content modelling and handling functionalities.
    Additionally, it uses the <a title="Repository" href="https://github.com/openeuropa/rdf_skos">OpenEuropa RDF SKOS component</a> to integrate the Publications Office (OP) vocabularies.
    </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_content"><img src="https://img.shields.io/packagist/v/openeuropa/oe_content.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_content"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_content/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_content"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_content.svg"/></a>
        </td> </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_corporate_blocks"><b>OpenEuropa Corporate Blocks</b></a><br/>
            This simple component contains the European Commission corporate blocks meant to display standardised parts of EC sites, such as the footer. It integrates with the <a title="Repository" href="https://github.com/openeuropa/oe_theme">OpenEuropa Theme</a> for styling.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_corporate_blocks"><img src="https://img.shields.io/packagist/v/openeuropa/oe_corporate_blocks.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_corporate_blocks"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_corporate_blocks/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_corporate_blocks"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_corporate_blocks.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/drupal-module-template"><b>OpenEuropa Drupal Module Template</b></a><br/>
            Builds the default files for a component to be used with the OpenEuropa project.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/drupal-module-template"><img src="https://img.shields.io/packagist/v/openeuropa/drupal-module-template.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/drupal-module-template"><img src="https://drone.fpfis.eu/api/badges/openeuropa/drupal-module-template/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/drupal-module-template"><img src="https://img.shields.io/packagist/dt/openeuropa/drupal-module-template.svg"/></a>
        </td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_editorial"><b>OpenEuropa Editorial</b></a><br/>
            This component provides various editorial features (workflow, versioning, etc), shipped as indiviual submodules. 
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_editorial"><img src="https://img.shields.io/packagist/v/openeuropa/oe_editorial.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_editorial"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_editorial/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_editorial"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_editorial.svg"/></a>
        </td> 
        </tr>
    <tr>
            <td>
                <a title="Repository" href="https://github.com/openeuropa/oe_link_lists"><b>OpenEuropa Link Lists</b></a><br/>
                This component provides site building features that allow the creation of lists of links, external and to internal content, dyanamic and manual.
            </td>
            <td width="250">
                <a title="Version" href="https://packagist.org/packages/openeuropa/oe_link_lists"><img src="https://img.shields.io/packagist/v/openeuropa/oe_link_lists.svg"/></a>
                <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_link_lists"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_link_lists/status.svg"/></a>
                <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_link_lists"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_link_lists.svg"/></a>
            </td> 
        </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_media"><b>OpenEuropa Media</b></a><br/>
            This component provides functionality for using Media of various types. Things like images, remote videos and integration with the EC AV Portal service are included.
            </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_media"><img src="https://img.shields.io/packagist/v/openeuropa/oe_media.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_media"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_media/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_media"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_media.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_multilingual"><b>OpenEuropa Multilingual</b></a><br/>
            This component provides EC corporate multilingual features such as the official EU languages, language switcher, language negotiation, etc.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_multilingual"><img src="https://img.shields.io/packagist/v/openeuropa/oe_multilingual.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_multilingual"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_multilingual/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_multilingual"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_multilingual.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_paragraphs"><b>OpenEuropa Paragraphs</b></a><br/>
            This component provides various Drupal paragraph types meant that display using the ECL components via the <a title="Repository" href="https://github.com/openeuropa/oe_theme">OpenEuropa Theme</a>.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_paragraphs"><img src="https://img.shields.io/packagist/v/openeuropa/oe_paragraphs.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_paragraphs"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_paragraphs/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_paragraphs"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_paragraphs.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_profile"><b>OpenEuropa Profile</b></a><br/>
            A basic installation profile that can be used for sites that use OpenEuropa components.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_profile"><img src="https://img.shields.io/packagist/v/openeuropa/oe_profile.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_profile"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_profile/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_profile"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_profile.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/rdf_skos"><b>OpenEuropa RDF SKOS</b></a><br/>
            An <a href="https://www.drupal.org/project/rdf_entity" target="_blank">RDF Entity</a> based implementation for SKOS vocabularies located in triple stores. This can be used for integrating the taxonomies provided by the EC Publications Office (OP). See also the <a title="Repository" href="https://github.com/openeuropa/oe_content">OpenEuropa Content</a> component.
        </td>
        <td>
            <a title="Version" href="https://packagist.org/packages/openeuropa/rdf_skos"><img src="https://img.shields.io/packagist/v/openeuropa/rdf_skos.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/rdf_skos"><img src="https://drone.fpfis.eu/api/badges/openeuropa/rdf_skos/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/rdf_skos"><img src="https://img.shields.io/packagist/dt/openeuropa/rdf_skos.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_search"><b>OpenEuropa Search</b></a><br/>
            This component provides corporate search functionalities.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_search"><img src="https://img.shields.io/packagist/v/openeuropa/oe_search.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_search"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_search/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_search"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_search.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_theme"><b>OpenEuropa Theme</b></a><br/>
            Drupal 8 theme based on the Europa Component Library.
        </td>
        <td>
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_theme"><img src="https://img.shields.io/packagist/v/openeuropa/oe_theme.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_theme"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_theme/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_theme"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_theme.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_translation"><b>OpenEuropa Translation</b></a><br/>
            This component provides translation capabilities for multilingual sites and integrations with various external translation services such as DGT Poetry.
        </td>
        <td>
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_translation"><img src="https://img.shields.io/packagist/v/openeuropa/oe_translation.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_translation"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_translation/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_translation"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_translation.svg"/></a>
        </td></tr>
    <tr>
    <td>
        <a title="Repository" href="https://github.com/openeuropa/oe_webtools"><b>OpenEuropa Webtools</b></a><br/>
        This component provides integration with the EC Webtools service for various widgets and functionalities such as analytics, LACO, cookie consent, etc. 
    </td>
    <td width="250">
        <a title="Version" href="https://packagist.org/packages/openeuropa/oe_webtools"><img src="https://img.shields.io/packagist/v/openeuropa/oe_webtools.svg"/></a>
        <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_webtools"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_webtools/status.svg"/></a>
        <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_webtools"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_webtools.svg"/></a>
    </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_time_caching"><b>OpenEuropa Time Caching</b></a><br/>
            The OpenEuropa Time Caching provides a cache tag service to generate and invalidate cache tags that deal with time.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_time_caching"><img src="https://img.shields.io/packagist/v/openeuropa/oe_time_caching.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_time_caching"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_time_caching/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_time_caching"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_time_caching.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_oembed"><b>OpenEuropa oEmbed</b></a><br/>
            The OpenEuropa oEmbed module allows the embedding of entities into content in an agnostic (non-Drupal) way.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_oembed"><img src="https://img.shields.io/packagist/v/openeuropa/oe_oembed.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_oembed"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_oembed/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_oembed"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_oembed.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/open_vocabularies"><b>Open Vocabularies</b></a><br/>
            The Open Vocabularies module allows users to choose how a piece of content will be categorised without having to change the related content type field definition.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/open_vocabularies"><img src="https://img.shields.io/packagist/v/openeuropa/open_vocabularies.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/open_vocabularies"><img src="https://drone.fpfis.eu/api/badges/openeuropa/open_vocabularies/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/open_vocabularies"><img src="https://img.shields.io/packagist/dt/openeuropa/open_vocabularies.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_corporate_site_info"><b>OpenEuropa Corporate Site Information</b></a><br/>
            The OpenEuropa Corporate Site Information module provides corporate information about the site, such as site owner, content owners, etc.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_corporate_site_info"><img src="https://img.shields.io/packagist/v/openeuropa/oe_corporate_site_info.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_corporate_site_info"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_corporate_site_info/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_corporate_site_info"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_corporate_site_info.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_newsroom"><b>OpenEuropa Newsroom</b></a><br/>
            The OpenEuropa oe_newsroom provides integration with the Newsroom service.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_newsroom"><img src="https://img.shields.io/packagist/v/openeuropa/oe_newsroom.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_newsroom"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_newsroom/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_newsroom"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_newsroom.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_graphql"><b>OpenEuropa GraphQL</b></a><br/>
            GraphQL integration module for OpenEuropa components, based on the <a href="https://www.drupal.org/project/graphql_core_schema">GraphQL Core Schema</a> module.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_graphql"><img src="https://img.shields.io/packagist/v/openeuropa/oe_graphql.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_graphql"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_graphql/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_graphql"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_graphql.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_agenda"><b>OpenEuropa Agenda</b></a><br/>
            Drupal module that exposes an agenda. The module defines the Agenda, Day, and Session sub-entity types and their default bundles.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_agenda"><img src="https://img.shields.io/packagist/v/openeuropa/oe_agenda.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_agenda"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_agenda/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_agenda"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_agenda.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_starter_content"><b>OpenEuropa Starter Content</b></a><br/>
            The OpenEuropa Starter Content provides a series of content types to quickstart a project.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_starter_content"><img src="https://img.shields.io/packagist/v/openeuropa/oe_starter_content.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_starter_content"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_starter_content/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_starter_content"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_starter_content.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_content_extra"><b>OpenEuropa Content Extra</b></a><br/>
            Enhances the basic <a href="https://github.com/openeuropa/oe_content">OpenEuropa Content</a> module with additional fields and entity types.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_content_extra"><img src="https://img.shields.io/packagist/v/openeuropa/oe_content_extra.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_content_extra"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_content_extra/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_content_extra"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_content_extra.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_subscriptions"><b>OpenEuropa Subscriptions</b></a><br/>
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_subscriptions"><img src="https://img.shields.io/packagist/v/openeuropa/oe_subscriptions.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_subscriptions"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_subscriptions/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_subscriptions"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_subscriptions.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_bootstrap_theme"><b>OpenEuropa Bootstrap base theme</b></a><br/>
            Drupal theme based on Bootstrap 5, UI Patterns and the <a href="https://github.com/openeuropa/bootstrap-component-library">OpenEuropa Bootstrap Component Library</a>.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_bootstrap_theme"><img src="https://img.shields.io/packagist/v/openeuropa/oe_bootstrap_theme.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_bootstrap_theme"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_bootstrap_theme/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_bootstrap_theme"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_bootstrap_theme.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_whitelabel"><b>OpenEuropa Whitelabel theme</b></a><br/>
            Sub-theme of <a href="https://packagist.org/packages/openeuropa/oe_bootstrap_theme">OpenEuropa Bootstrap base theme</a>, with theming for OpenEuropa library features.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_whitelabel"><img src="https://img.shields.io/packagist/v/openeuropa/oe_whitelabel.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_whitelabel"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_whitelabel/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_whitelabel"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_whitelabel.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_showcase"><b>OpenEuropa Showcase</b></a><br/>
            Installation profile to demo openeuropa library features.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_showcase"><img src="https://img.shields.io/packagist/v/openeuropa/oe_showcase.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_showcase"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_showcase/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_showcase"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_showcase.svg"/></a>
        </td></tr>
</table>

### PHP projects

<table>
    <tr>
        <th>Component</th>
        <th>Status</th>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/behat-transformation-context"><b>Behat Transformation Context</b></a><br/>
            This package provides a Behat context allowing to transform human readable labels to selectors or page paths.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/behat-transformation-context"><img src="https://img.shields.io/packagist/v/openeuropa/behat-transformation-context.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/behat-transformation-context"><img src="https://drone.fpfis.eu/api/badges/openeuropa/behat-transformation-context/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/behat-transformation-context"><img src="https://img.shields.io/packagist/dt/openeuropa/behat-transformation-context.svg"/></a></td>
        </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/code-review"><b>Code Review</b></a><br/>
            Automated quality assurance checks based on GrumPHP.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/code-review"><img src="https://img.shields.io/packagist/v/openeuropa/code-review.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/code-review"><img src="https://drone.fpfis.eu/api/badges/openeuropa/code-review/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/code-review"><img src="https://img.shields.io/packagist/dt/openeuropa/code-review.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/code-review-drupal"><b>Code Review Drupal</b></a><br/>
            Extends the Code Review with Drupal based rules.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/code-review-drupal"><img src="https://img.shields.io/packagist/v/openeuropa/code-review-drupal.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/code-review-drupal"><img src="https://drone.fpfis.eu/api/badges/openeuropa/code-review-drupal/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/code-review-drupal"><img src="https://img.shields.io/packagist/dt/openeuropa/code-review-drupal.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/code-review-library"><b>Code Review Library</b></a><br/>
            Coding standard dependencies for PHP libraries.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/code-review-library"><img src="https://img.shields.io/packagist/v/openeuropa/code-review-library.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/code-review-library"><img src="https://drone.fpfis.eu/api/badges/openeuropa/code-review-library/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/code-review-library"><img src="https://img.shields.io/packagist/dt/openeuropa/code-review-library.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/composer-artifacts"><b>Composer artifacts</b></a><br/>
            Composer plugin that allows to download a specified artifact instead of the project source.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/composer-artifacts"><img src="https://img.shields.io/packagist/v/openeuropa/composer-artifacts.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/composer-artifacts"><img src="https://drone.fpfis.eu/api/badges/openeuropa/composer-artifacts/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/composer-artifacts"><img src="https://img.shields.io/packagist/dt/openeuropa/composer-artifacts.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/drupal-core-require-dev"><b>Drupal Core require dev</b></a><br/>
            This package provides the require dependencies of drupal/core as a standalone package.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/drupal-core-require-dev"><img src="https://img.shields.io/packagist/v/openeuropa/drupal-core-require-dev.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/drupal-core-require-dev"><img src="https://drone.fpfis.eu/api/badges/openeuropa/drupal-core-require-dev/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/drupal-core-require-dev"><img src="https://img.shields.io/packagist/dt/openeuropa/drupal-core-require-dev.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/ecl-twig-loader"><b>ECL Twig loader</b></a><br/>
            Twig loader for Europa Component Library, it allows to load components by accessing them via a configurable ecl-twig-loaderspace.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/ecl-twig-loader"><img src="https://img.shields.io/packagist/v/openeuropa/ecl-twig-loader.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/ecl-twig-loader"><img src="https://drone.fpfis.eu/api/badges/openeuropa/ecl-twig-loader/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/ecl-twig-loader"><img src="https://img.shields.io/packagist/dt/openeuropa/ecl-twig-loader.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/task-runner"><b>Task Runner</b></a><br/>
            PHP task runner based on Robo, focused on extensibility.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/task-runner"><img src="https://img.shields.io/packagist/v/openeuropa/task-runner.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/task-runner"><img src="https://drone.fpfis.eu/api/badges/openeuropa/task-runner/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/task-runner"><img src="https://img.shields.io/packagist/dt/openeuropa/task-runner.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/webtools-geocoding-provider"><b>Webtools Geolocation provider</b></a><br/>
            This is a provider for the Geocoder PHP library that integrates the Webtools Geolocation service from the European Commission.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/webtools-geocoding-provider"><img src="https://img.shields.io/packagist/v/openeuropa/webtools-geocoding-provider.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/webtools-geocoding-provider"><img src="https://drone.fpfis.eu/api/badges/openeuropa/webtools-geocoding-provider/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/webtools-geocoding-provider"><img src="https://img.shields.io/packagist/dt/openeuropa/webtools-geocoding-provider.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/europa-search-client"><b>Europa Search Client</b></a><br/>
            Europa Search Client is a library offering a PHP API to consume Europa Search services.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/europa-search-client"><img src="https://img.shields.io/packagist/v/openeuropa/europa-search-client.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/europa-search-client"><img src="https://drone.fpfis.eu/api/badges/openeuropa/europa-search-client/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/europa-search-client"><img src="https://img.shields.io/packagist/dt/openeuropa/europa-search-client.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/triple-store-dev"><b>Content layer development triple store</b></a><br/>
            Triple storage containing default data to kick-start content layer local development based on <a href="https://virtuoso.openlinksw.com">OpenLink Virtuoso</a>.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/triple-store-dev"><img src="https://img.shields.io/packagist/v/openeuropa/triple-store-dev.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/triple-store-dev"><img src="https://drone.fpfis.eu/api/badges/openeuropa/triple-store-dev/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/triple-store-dev"><img src="https://img.shields.io/packagist/dt/openeuropa/triple-store-dev.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/epoetry-client"><b>ePoetry PHP client</b></a><br/>
            PHP client for the ePoetry service.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/epoetry-client"><img src="https://img.shields.io/packagist/v/openeuropa/epoetry-client.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/epoetry-client"><img src="https://drone.fpfis.eu/api/badges/openeuropa/epoetry-client/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/epoetry-client"><img src="https://img.shields.io/packagist/dt/openeuropa/epoetry-client.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/epoetry-client"><b>ePoetry PHP client</b></a><br/>
            PHP client for the ePoetry service.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/epoetry-client"><img src="https://img.shields.io/packagist/v/openeuropa/epoetry-client.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/epoetry-client"><img src="https://drone.fpfis.eu/api/badges/openeuropa/epoetry-client/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/epoetry-client"><img src="https://img.shields.io/packagist/dt/openeuropa/epoetry-client.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/task-runner-drupal-project-symlink"><b>OpenEuropa Task Runner: Drupal project symlink</b></a><br/>
            The Drupal project symlink <a href="https://github.com/openeuropa/task-runner">"Task Runner</a> command aims at simplifying Drupal development, when using a Composer-based workflow.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/task-runner-drupal-project-symlink"><img src="https://img.shields.io/packagist/v/openeuropa/task-runner-drupal-project-symlink.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/task-runner-drupal-project-symlink"><img src="https://drone.fpfis.eu/api/badges/openeuropa/task-runner-drupal-project-symlink/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/task-runner-drupal-project-symlink"><img src="https://img.shields.io/packagist/dt/openeuropa/task-runner-drupal-project-symlink.svg"/></a>
        </td></tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/cdt-client"><b>OpenEuropa CDT Client</b></a><br/>
            CDT Client is a library offering a PHP API to consume Translation Centre For the Bodies of the EU services.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/cdt-client"><img src="https://img.shields.io/packagist/v/openeuropa/cdt-client.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/task-runner-drupal-project-symlink"><img src="https://drone.fpfis.eu/api/badges/openeuropa/cdt-client/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/cdt-client"><img src="https://img.shields.io/packagist/dt/openeuropa/cdt-client.svg"/></a>
        </td></tr>
</table>

[1]: http://www.php-fig.org
[2]: http://www.phptherightway.com
[3]: https://packagist.org/packages/openeuropa/
[4]: https://joinup.ec.europa.eu/page/eupl-text-11-12
