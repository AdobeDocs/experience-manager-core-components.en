---
title: it.tests Module of AEM Project Archetype
description: How to use the AEM Project Archetype Integration Tests
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Administrator
---

# it.tests Module of the AEM Project Archetype {#ittests-module}

There are three levels of testing contained in the project:

* [Unit Tests](core.md#unit-tests)
* Integration Tests
* [UI Tests](uitests.md)

This article describes the integration tests available as part of the it.tests module.

## Running Integration Tests {#running-tests}

The server-side integration tests allow unit-like tests to be run in the AEM-environment, i.e. on the AEM server. To test, execute:

```
mvn clean verify -PintegrationTests
```
