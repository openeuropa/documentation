# Development workflow

## Governance

OpenEuropa is a project owned and maintained by the European Commission's DG DIGIT.

OpenEuropa components and features are created for European Commission internal web projects,
but they are made as generic as possible and released as [Open Source Software](https://github.com/openeuropa/openeuropa/blob/master/LICENCE.txt)
so they can also be used in other projects and receive contributions from the Open Source Community (hereinafter referred to as "external contributors").

DG DIGIT's OpenEuropa Core team is in charge of OpenEuropa developments and maintenance, under the supervision of its Product Owner,
who decides on the priorities, depending on European Commission needs.

While the OpenEuropa team strongly welcomes and encourages contributions, European Commission projects have the priority over external entities needs,
which means an external contribution or support request might be handled after a certain period of time, depending on available resources,
or might be rejected at the sole discretion of the OpenEuropa team representatives (hereinafter referred to as "maintainers").

## OpenEuropa contribution rules

Contributions are governed by [OpenEuropa contribution guidelines](../initiative/how-to-contribute).

## Lifecycle of proposed issues

All contributed issues, both bug reports and feature requests, are handled as GitHub issues.
This allows external contributors to follow up on the progress without the need to access DIGIT's internal ticketing system.

Contributed issues are regularly examined by the maintainers of the repository they were created in.
Maintainers are able to decide whether the contributed issue has value or not, in which case it will be duplicated into an internal ticket
in order to be able to track resources and deal with internal comments.

Although there is no set of rules defining if an issue has value to the OpenEuropa project, here is a set of guidelines:

* The issue reports a critical bug that renders the component unusable.
* The issue reports a bug that is clear and is unmistakably the component's fault.
* The issue requests a feature that was described in the component but not provided.
* The issue requests a modification that does not break backwards compatibility.
* The issue requests a feature without which the component is unusable.

Maintainers are advised to use their know-how and best common sense to filter these issues to the best of their capabilities.

Once the issues have been moved to an internal ticket, the maintainers have to decide together with the OpenEuropa Product Owner on the priority of issues,
after which the tickets are handled following the usual development workflow of all OpenEuropa tickets (which itself is based on Agile methodologies).

Information on the progress has to be regularly added in the associated GitHub ticket as well, in order for the external contributor(s) to be kept informed.

## Lifecycle of proposed pull requests

All contributed pull requests are to be created together with a related GitHub issue.
These issues follow the lifecycle described above, regardless of whether the pull request was created together with the issue or not.

In the case the issue was created together with a pull request or the issue has not been examined yet, the issue is handled as described above
and the related internal ticket has to be reviewed. It is the responsibility of the contributor to handle any required modification to the proposed code.

In the case the pull request is created in a later state and the related internal ticket is already available,
the proposed pull request is evaluated as part of the development of the ticket, and it is the responsibility of the developer in charge of the ticket
to handle any required modification to the proposed code.
