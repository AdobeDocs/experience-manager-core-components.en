---
title: Core Module of the AEM Project Archetype
seo-title: Core Module of the AEM Project Archetype
description: Core Module of the AEM Project Archetype
seo-description: Core Module of the AEM Project Archetype
contentOwner: bohnert
content-type: reference
topic-tags: authoring
topic-tags: core-components
---

# Core Module of the AEM Project Archetype {#core-module}

The core maven module (`<src-directory>/<project>/core`) includes all the Java code needed for the implementation. The module will package all of the Java code and deploy to the AEM instance as an OSGi Bundle.

The Maven Bundle Plugin defined in the `<src-directory>/<project>/core/pom.xml` is responsible for compiling the Java code into an OSGi bundle that can be recognized by AEM's OSGi container. Note that this is where the location of Sling Models are defined.

Although it is rare that the core bundle needs to be deployed independently of the ui.apps module in upper level environments, deploying the core bundle directly is useful during local development/testing. The Maven Sling Plugin allows the core bundle to be deployed to AEM directly leveraging the `autoInstallBundle` profile as defined in the [parent POM](archetype.md#parent-pom).

```
mvn -PautoInstallBundle clean install
```

Once successfully executed, you should be able to see the Bundels Console at `http://<host>:<port>/system/console/bundles`.
