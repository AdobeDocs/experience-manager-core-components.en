---
title: ui.tests Module of AEM Project Archetype
description: How to use the AEM Project Archetype UI Tests
feature: "Core Components, AEM Project Archetype"
role: "Architect, Developer, Administrator"
---

# ui.tests Module of the AEM Project Archetype {#uitests-module}

There are three levels of testing contained in the project:

* [Unit Tests](core.md#unit-tests)
* [Integration Tests](ittests.md)
* UI Tests

This article describes the UI tests available as part of the ui.tests module.

## Running UI Tests {#running-tests}

To test, execute:

```shell
mvn verify -Pui-tests-local-execution
```

After execution, reports and logs are available in the `target/reports` folder.

## Additional Options {#additional-options}

UI tests can be run with many different options including for headless testing against a local browser and as a Docker image. See the [README.md file of the ui.tests module](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests) for further information.
