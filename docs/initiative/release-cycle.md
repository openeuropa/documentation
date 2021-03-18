# OpenEuropa Release Cycle
This document explains the release process followed by OpenEuropa project for its components.
OpenEuropa releases its component following semantic versioning (https://semver.org/)

There are three types of releases: 

- **MAJOR**: Incompatible API changes, very rare and planned in. 
- **MINOR**: Adds backwards-compatible manner functionalities and bug fixes.
- **PATCH**: Adds backwards-compatible bug/security fixes and can be deployed instantaneously. No new functionality will be introduced.

OpenEuropa components release plan don't follow a fixed overall timeline and can happen in different planned slots. Each component roadmap and release plan will be made available to the public.

## Release preparation and testing

The OpenEuropa team commits to have its components aligned with the API of the supported Drupal versions.

It is predicted that the majority of changes will come in the form of MINOR and PATCH releases. However, if there is a need to change API provided by the component in a way that it is not backwards compatible a new MAJOR release can be produced. 

Each OpenEuropa component defines in its dependencies the minimum requirements for components version it depends upon. Each minor version can have development, beta, and release candidate phases.

## Release support

For Drupal components, OpenEuropa team have a support policy inspired by Drupal core:
- Components support current and previous Drupal Core minor versions. New minor versions for components are made compatible with these respective core versions.
- When a new minor core version (n) is supported, the support for release n-2 is dropped. 

This follows a similar release cycle proposed for Drupal Core from a security standpoint and guarantees that all users of OpenEuropa components are running current minor release of supported Drupal Core (n) or previous (n-1).
As Drupal core minor releases happen every 6 months, website and application owners should be prepared to update to every minor release at least every 6 months.

## Backwards compatibility

Our Backward Compatibility Promise allows developers to upgrade with confidence from one minor version to the next one. Whenever keeping backward compatibility is not possible, the feature, the enhancement or the bug fix will be scheduled for the next major version.

## Deprecation policy

New minor versions can introduce new APIs and new features. When a new API replaces an old one, the later cannot be
removed because it would break the backwards compatibility pledge. Instead, the old API will be deprecated in favor of
the new one.

### How to deprecate

A deprecation consists of two parts:

* A `@deprecated` PHPDoc tag that indicates when the code was deprecated, when it will be removed, and what to use
  instead. An optional `@see` link to a relevant issue, explaining the API change.
* A `@trigger_error('...', E_USER_DEPRECATED)` at runtime to notify developers that deprecated code is being used. The
  `@` suppression should be used in most cases so that we can customize the error handling and avoid flooding logs on
  production. In some cases, we will omit the `@` if it is important to notify developers of a behavior or BC break
  (e.g. for a critical issue).

Additionally, developers and QA may consider adding a third part: A unit test proving the deprecation notice will be
triggered when the deprecated code is called. Use a `@group` legacy annotation in conjunction with calls to
`$this->expectDeprecation()`.

Note that Drupal deprecation message template is very coupled to Drupal core and contrib use-cases and it doesn't fit
the OpenEuropa components case, but it's important that the message contain all the elements described above.

### What to deprecate

OpenEuropa is following the Drupal's Deprecation Policy regarding what is
subject to deprecation: https://www.drupal.org/about/core/policies/core-change-policies/drupal-core-deprecation-policy#what

## References

* [Drupal core release cycle: major, minor, and patch releases](https://www.drupal.org/core/release-cycle-overview)
* [Drupal core deprecation policy](https://www.drupal.org/about/core/policies/core-change-policies/drupal-core-deprecation-policy)
