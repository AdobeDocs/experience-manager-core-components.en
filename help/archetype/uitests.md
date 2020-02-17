---
title: ui.tests Module of AEM Project Archetype
description: How to use the AEM Project Archetype JUnit Tests
---

# ui.tests Module of the AEM Project Archetype {#uitests-module}

There are three levels of testing contained in the project:

## Unit Tests {#unit-tests}

The unit test in the [core module](core.md) showcases classic unit testing of the code contained in the bundle. To test, execute:

```
mvn clean test
```

## Integration Tests {#integration-tests}

The server-side integration tests allow unit-like tests to be run in the AEM-environment, i.e. on the AEM server. To test, execute:

```
mvn clean verify -PintegrationTests
```

## Client-Side Tests {#client-side-tests}

The `client-side Hobbes.js` tests  are JavaScript-based browser-side tests that verify browser-side behavior.

To test, when viewing an AEM page you want to test in the browser, open the page in **Developer mode** by opening the left panel and switch to the **Tests** tab and find the generated **MyName Tests** and run them.
