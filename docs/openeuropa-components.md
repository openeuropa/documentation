# OpenEuropa components

Below the list of loosely coupled, reusable PHP projects provided by the OpenEuropa Initiative.
Each project complies with [PHP-FIG][1] standards and adhere to the best-practices put forward by [PHP The "Right" Way][2].

All code is distributed on [Packagist][3] and released under the [EUPL-1.2 license][4].

All projects use Semantic Versioning. Attention is drawn to [item 4 of the Semantic Versioni specification](https://semver.org/#spec-item-4)
'Major version zero (0.y.z) is for initial development. Anything may change at any time. The public API should not be considered stable.'

### PHP projects

<table>
    <tr>
        <th>Component</th>
        <th>Status</th>
        <th>Maintainers</th>
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
        <td><a href="https://github.com/voidtek">Victor Da Costa</a><br/>
            <a href="https://github.com/dxvargas">Diogo Vargas</a></td>
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
        </td>
 <td><a href="https://github.com/drupol">Pol Dellaiera</a><br/>
            <a href="https://github.com/pfrenssen">Pieter Frenssen</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/composer-artifacts"><b>Composer artifacts</b></a><br/>
            Composer plugin that allows to download a specified artifact instead of the project source.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/composer-artifacts"><img src="https://img.shields.io/packagist/v/openeuropa/composer-artifacts.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/composer-artifacts"><img src="https://drone.fpfis.eu/api/badges/openeuropa/composer-artifacts/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/composer-artifacts"><img src="https://img.shields.io/packagist/dt/openeuropa/composer-artifacts.svg"/></a>
        </td>
 <td><a href="https://github.com/voidtek">Victor Da Costa</a><br/>
            <a href="https://github.com/drupol">Pol Dellaiera</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/drupal-core-require-dev"><b>Drupal Core require dev</b></a><br/>
            This package provides the require dependencies of drupal/core as a standalone package.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/drupal-core-require-dev"><img src="https://img.shields.io/packagist/v/openeuropa/drupal-core-require-dev.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/drupal-core-require-dev"><img src="https://drone.fpfis.eu/api/badges/openeuropa/drupal-core-require-dev/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/drupal-core-require-dev"><img src="https://img.shields.io/packagist/dt/openeuropa/drupal-core-require-dev.svg"/></a>
        </td>
 <td><a href="https://github.com/voidtek">Victor Da Costa</a><br/>
            <a href="https://github.com/drupol">Pol Dellaiera</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/ecl-twig-loader"><b>ECL Twig loader</b></a><br/>
            Twig loader for Europa Component Library, it allows to load components by accessing them via a configurable ecl-twig-loaderspace.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/ecl-twig-loader"><img src="https://img.shields.io/packagist/v/openeuropa/ecl-twig-loader.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/ecl-twig-loader"><img src="https://drone.fpfis.eu/api/badges/openeuropa/ecl-twig-loader/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/ecl-twig-loader"><img src="https://img.shields.io/packagist/dt/openeuropa/ecl-twig-loader.svg"/></a>
        </td>
 <td><a href="https://github.com/ademarco">Antonio De Marco</a><br/>
            <a href="https://github.com/sergepavle">Sergii Pavlenko</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/task-runner"><b>Task Runner</b></a><br/>
            PHP task runner based on Robo, focused on extensibility.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/task-runner"><img src="https://img.shields.io/packagist/v/openeuropa/task-runner.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/task-runner"><img src="https://drone.fpfis.eu/api/badges/openeuropa/task-runner/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/task-runner"><img src="https://img.shields.io/packagist/dt/openeuropa/task-runner.svg"/></a>
        </td>
 <td><a href="https://github.com/drupol">Pol Dellaiera</a><br/>
            <a href="https://github.com/pfrenssen">Pieter Frenssen</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/webtools-geocoding-provider"><b>Webtools Geolocation provider</b></a><br/>
            This is a provider for the Geocoder PHP library that integrates the Webtools Geolocation service from the European Commission.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/webtools-geocoding-provider"><img src="https://img.shields.io/packagist/v/openeuropa/webtools-geocoding-provider.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/webtools-geocoding-provider"><img src="https://drone.fpfis.eu/api/badges/openeuropa/webtools-geocoding-provider/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/webtools-geocoding-provider"><img src="https://img.shields.io/packagist/dt/openeuropa/webtools-geocoding-provider.svg"/></a>
        </td>
 <td><a href="https://github.com/drupol">Pol Dellaiera</a><br/>
            <a href="https://github.com/pfrenssen">Pieter Frenssen</a></td>
    </tr>
</table>

### Drupal projects

<table>
    <tr>
        <th>Component</th>
        <th>Status</th>
        <th>Maintainers</th>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_authentication"><b>OpenEuropa Authentication</b></a><br/>
            This module allows to authenticate users against the European Commission login service.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_authentication"><img src="https://img.shields.io/packagist/v/openeuropa/oe_authentication.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_authentication"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_authentication/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_authentication"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_authentication.svg"/></a>
        </td>
 <td><a href="https://github.com/imanoleguskiza">Imanol Eguskiza</a><br/>
            <a href="https://github.com/dxvargas">Diogo Vargas</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_content"><b>OpenEuropa Content</b></a><br/>
            A Drupal module that contains the corporate entity types in Drupal.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_content"><img src="https://img.shields.io/packagist/v/openeuropa/oe_content.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_content"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_content/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_content"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_content.svg"/></a>
        </td>
 <td><a href="https://github.com/nagyad">Adam</a><br/>
            <a href="https://github.com/brummbar">Francesco</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_corporate_blocks"><b>OpenEuropa Corporate Blocks</b></a><br/>
            A Drupal module that contains the OpenEuropa Corporate Blocks in Drupal.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_corporate_blocks"><img src="https://img.shields.io/packagist/v/openeuropa/oe_corporate_blocks.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_corporate_blocks"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_corporate_blocks/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_corporate_blocks"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_corporate_blocks.svg"/></a>
        </td>
 <td><a href="https://github.com/nagyad">Adam</a><br/></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/drupal-module-template"><b>OpenEuropa Drupal Module Template</b></a><br/>
            Builds the default files for a module to be used with the OpenEuropa project.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/drupal-module-template"><img src="https://img.shields.io/packagist/v/openeuropa/drupal-module-template.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/drupal-module-template"><img src="https://drone.fpfis.eu/api/badges/openeuropa/drupal-module-template/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/drupal-module-template"><img src="https://img.shields.io/packagist/dt/openeuropa/drupal-module-template.svg"/></a>
        </td>
 <td><a href="https://github.com/dxvargas">Diogo Vargas</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_editorial"><b>OpenEuropa Editorial</b></a><br/>
            Editorial features for the OpenEuropa project.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_editorial"><img src="https://img.shields.io/packagist/v/openeuropa/oe_editorial.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_editorial"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_editorial/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_editorial"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_editorial.svg"/></a>
        </td>
 <td><a href="https://github.com/nagyad">Adam</a><br/>
            <a href="https://github.com/hernani">hernani</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_media"><b>OpenEuropa Media</b></a><br/>
            The OpenEuropa Media module provides functionality for inclusion of Media on sites.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_media"><img src="https://img.shields.io/packagist/v/openeuropa/oe_media.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_media"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_media/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_media"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_media.svg"/></a>
        </td>
 <td><a href="https://github.com/sergepavle">Sergii Pavlenko</a><br/>
            <a href="https://github.com/upchuk">Daniel Sipos</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_multilingual"><b>OpenEuropa Multilingual</b></a><br/>
            Multilingual features for the OpenEuropa project.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_multilingual"><img src="https://img.shields.io/packagist/v/openeuropa/oe_multilingual.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_multilingual"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_multilingual/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_multilingual"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_multilingual.svg"/></a>
        </td>
 <td><a href="https://github.com/voidtek">Victor Da Costa</a><br/>
            <a href="https://github.com/dxvargas">Diogo Vargas</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_paragraphs"><b>OpenEuropa Paragraphs</b></a><br/>
            This module integrates the ECL, the component library of the European Commission, with the Paragraphs module.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_paragraphs"><img src="https://img.shields.io/packagist/v/openeuropa/oe_paragraphs.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_paragraphs"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_paragraphs/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_paragraphs"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_paragraphs.svg"/></a>
        </td>
 <td><a href="https://github.com/nagyad">Adam</a><br/>
            <a href="https://github.com/brummbar">Francesco</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_profile"><b>OpenEuropa Profile</b></a><br/>
            Drupal profile for the OpenEuropa project.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_profile"><img src="https://img.shields.io/packagist/v/openeuropa/oe_profile.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_profile"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_profile/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_profile"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_profile.svg"/></a>
        </td>
 <td><a href="https://github.com/ademarco">Antonio De Marco</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/rdf_skos"><b>OpenEuropa RDF SKOS</b></a><br/>
            A SKOS implementation for RDF entity
        </td>
        <td>
            <a title="Version" href="https://packagist.org/packages/openeuropa/rdf_skos"><img src="https://img.shields.io/packagist/v/openeuropa/rdf_skos.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/rdf_skos"><img src="https://drone.fpfis.eu/api/badges/openeuropa/rdf_skos/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/rdf_skos"><img src="https://img.shields.io/packagist/dt/openeuropa/rdf_skos.svg"/></a>
        </td>
 <td><a href="https://github.com/upchuk">Daniel Sipos</a><br/>
            <a href="https://github.com/brummbar">Francesco</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_search"><b>OpenEuropa Search</b></a><br/>
            Drupal profile for the OpenEuropa project.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_search"><img src="https://img.shields.io/packagist/v/openeuropa/oe_search.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_search"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_search/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_search"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_search.svg"/></a>
        </td>
 <td><a href="https://github.com/sergepavle">Sergii Pavlenko</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_theme"><b>OpenEuropa Theme</b></a><br/>
            Drupal 8 theme based on the Europa Component Library.
        </td>
        <td>
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_theme"><img src="https://img.shields.io/packagist/v/openeuropa/oe_theme.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_theme"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_theme/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_theme"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_theme.svg"/></a>
        </td>
 <td><a href="https://github.com/ademarco">Antonio De Marco</a><br/>
            <a href="https://github.com/sergepavle">Sergii Pavlenko</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_webtools"><b>OpenEuropa Webtools</b></a><br/>
            Drupal module providing webtools analytics integration such as Matomo (formerly PIWIK).
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_webtools"><img src="https://img.shields.io/packagist/v/openeuropa/oe_webtools.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_webtools"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_webtools/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_webtools"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_webtools.svg"/></a>
        </td>
 <td><a href="https://github.com/imanoleguskiza">Imanol Eguskiza</a><br/>
            <a href="https://github.com/upchuk">Daniel Sipos</a></td>
    </tr>
    <tr>
        <td>
            <a title="Repository" href="https://github.com/openeuropa/oe_webtools_location"><b>OpenEuropa Webtools Location Services</b></a><br/>
            Drupal module that provides integration with Webtools location services, such as geocoding and maps.
        </td>
        <td width="250">
            <a title="Version" href="https://packagist.org/packages/openeuropa/oe_webtools_location"><img src="https://img.shields.io/packagist/v/openeuropa/oe_webtools_location.svg"/></a>
            <a title="Build" href="https://drone.fpfis.eu/openeuropa/oe_webtools_location"><img src="https://drone.fpfis.eu/api/badges/openeuropa/oe_webtools_location/status.svg"/></a>
            <a title="Downloads" href="https://packagist.org/packages/openeuropa/oe_webtools_location"><img src="https://img.shields.io/packagist/dt/openeuropa/oe_webtools_location.svg"/></a>
        </td>
 <td><a href="https://github.com/pfrenssen">Pieter Frenssen</a><br/>
            <a href="https://github.com/drupol">Pol Dellaiera</a></td>
    </tr>
</table>

[1]: http://www.php-fig.org
[2]: http://www.phptherightway.com
[3]: https://packagist.org/packages/openeuropa/
[4]: https://joinup.ec.europa.eu/page/eupl-text-11-12
