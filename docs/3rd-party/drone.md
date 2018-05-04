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
* On many Linux based systems Docker is running as a service which means it has
  root access to the file system. Take precautions to not run untrusted
  containers, and be prepared to handle files being written as root into your
  working directory. There is a feature request to solve this in Drone (ref.
  https://github.com/drone/drone/issues/1492). You can also get in touch with
  your container maintainer to solve this on container level, e.g. by checking
  an environment variable `UID` and running as this user.
* We are currently using some containers that include an older version of the
  Linux kernel (more specifically, CentOS 6 which runs on the 2.6 kernel).
  There is an incompatibility that occurs when running these on a host OS that
  has a more kernel (4.15 or newer). The problem currently manifests itself
  with the container exiting with exit code 139. To solve this, run the host
  system with the kernel parameter `vsyscall=emulate`. See for example:
  https://bugs.archlinux.org/task/57336
