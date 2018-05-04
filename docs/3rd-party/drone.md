Drone
=====

OpenEuropa is using [Drone](https://drone.io/) for continuous integration and
continuous delivery.

Policies regarding the use of the FPFIS Drone service
-----------------------------------------------------

Ref. https://webgate.ec.europa.eu/CITnet/jira/browse/OPENEUROPA-571


Enabling Drone for a new repository
-----------------------------------

The repository should be enabled in the web interface at [Account >
Repositories](https://drone.fpfis.eu/account/repos). This action can only be
taken by the repository maintainer.

In the repository settings for the Drone application on Github the necessary
actions should then be configured, so that the tests will run on all branches,
ull requests, tags, etc.


Testing Drone in a local development environment
------------------------------------------------

* Install the Drone CLI tool, ref. [Drone CLI
  installation](http://docs.drone.io/cli-installation/).
* In the root folder of the repository (where the `.drone.yml` file is
  located), execute the Drone pipeline with:

    $ drone exec --local

* You can simulate any git events that might occur on the repository. Refer to
  the Drone CLI documentation for more information. For example to simulate new
  commits being pushed to the master branch:

    $ drone exec --build-event push --commit-branch master


### Tips regarding the use of the Drone CLI tool

* If the tool appears to 'hang' for a long time, it is probably downloading
  Docker containers in the background. Be patient. Ref.
  https://github.com/drone/drone-cli/issues/46.
* If you get unexpected errors, make sure your local checkout of the repository
  is clean. Remove folders such as `vendor/` and `npm_modules`, remove your
  local `runner.yml` file, etc. Ideally you should clone a brand new
  repository, since this is also what the Drone server is doing at the start of
  the process.
