# Code reviews

Pull Requests introducing changes in the Openeuropa components are manually reviewed.

The following aspects should be checked:
- Implementation follows the ticket instruction and the defined solution.
- Correct code split between components, and inside components correct split between services, plugins, .module file, and .install file.
- Prefixing on configuration provided.
- Type-hinting for code that is not inherited.
- Comments explain complex logic.
- Test cover introduced all introduced functionality.
