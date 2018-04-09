# Open Europa Release Cycle
This document explains the release process followed by Open Europa project for its components.
Open Europa releases its component following semantic versioning (https://semver.org/)

There will be three types of releases planned: 

- **MAJOR**: Incompatible API changes, very rare and planned in. 
- **MINOR**: Adds backwards-compatible manner functionalities and bug fixes.
- **PATCH**: Adds backwards-compatible bug / security fixes and can be deployed instantaneously. No new functionality will be introduced.

Open Europa components release plan will not follow a fixed overall timeline and can happen in different planned slots. Each component roadmap and release plan will be made available to public.

## Release preparation and testing

OpenEuropa Drupal components releases will follow Drupal 8 core releases and will always be tested against:
- Current stable Drupal 8 core minor release (n)
- Previous supported Drupal 8 core minor release (n-1)
- Development branch for next Drupal 8 core minor release 

This will allow to follow the same support cycle as Drupal core and be better prepared for next minor releases as they occur.

When a new Drupal core minor version is released, Open Europa team commits to have a release of all its supported components compatible with it in a fixed time frame (two sprints).

It is predicted that the majority of changes will come in the form of MINOR and PATCH releases. However if there is a need to change API provided by the component in a way that it is not backwards compatible a new MAJOR release can be produced. 

Each Open Europa component will define in its dependencies the minimum requirements for components version it depends upon. Each minor version can have development, beta, and release candidate phases.

## Release support

For Drupal components, Open Europa team will have a support policy inspired by Drupal core: 
- Components support current and previous Drupal Core minor versions. New minor versions for components are made compatible with these respective core versions.
- When a new minor core version (n) is supported, the support for release n-2 is dropped. 

This follows a similar release cycle proposed for Drupal Core from a security stand point and guarantees that all users of Open Europa components are running current minor release of supported Drupal Core (n) or previous (n-1).
As Drupal core minor releases happen every 6 months, website and application owners should be prepared to update to every minor release at least every 6 months.

## Backwards compatibility

Our Backward Compatibility Promise allows developers to upgrade with confidence from one minor version to the next one. Whenever keeping backward compatibility is not possible, the feature, the enhancement or the bug fix will be scheduled for the next major version.

## References
https://www.drupal.org/core/release-cycle-overview
