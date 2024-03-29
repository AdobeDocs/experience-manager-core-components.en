---
title: Using the AEM Project Archetype
description: Learn how to use the AEM Project Archetype to create a minimal, best-practices-based Adobe Experience Manager project as a starting point for your own AEM projects.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
---

# Using the AEM Project Archetype {#using-the-archetype}

This document explains how you can use the AEM Project Archetype to create a minimal, best-practices-based Adobe Experience Manager project as a starting point for your own AEM projects. 

It focuses on general usage patterns and what the archetype does for you. For detailed build options and technical instructions, please see the documentation in the GitHub repository of the archetype.

>[!TIP]
>
>The latest AEM Project Archetype and associated technical documentation [can be found on GitHub.](https://github.com/adobe/aem-project-archetype)

## Getting Started {#getting-started}

The project archetype makes it easy to get started developing on AEM. You can take your first steps with the archetype in a number of ways.

* **WKND Tutorial** - For a great introduction to developing on AEM including how to leverage the archetype see the [Getting Started with AEM Sites - WKND Tutorial](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) for a practical example that walks you through using the archetype to implement a simple project.
* **WKND Events Tutorial** - If you are particularly interested in single page application (SPA) development on AEM, be sure to check out dedicated [WKND Events tutorial.](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)
* **Start on your own!** - You can easily download the [current project archetype available on GitHub](https://github.com/adobe/aem-project-archetype) and create your first project on your own.

## How to Use the Archetype {#how-to-use-the-archetype}

The first step using the archetype is to create a project, which generates [the modules](#what-you-get) in a local file structure. As part of project generation, a number of properties for your project can be defined such as project name, version, enabling various options, etc.

>[!TIP]
>
>Whenever you build the archetype, it will also generate a series of readmes, providing you with the technical details and usage of each module as [linked below.](#what-you-get)

Building the project with Maven creates the artifacts (packages and OSGi bundles), that can be deployed to AEM. Additional Maven commands and profiles can be used to deploy the project artifacts to an AEM instance.

## What You Get Using the Archetype {#what-you-get}

The archetype is made up of modules, all of which are created automatically when using the archetype.

* **[core](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** is a Java bundle containing all core functionality like OSGi services, listeners, and schedulers, as well as component-related Java code such as servlets and request filters.
* **[it.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** are Java-based integration tests.
* **[ui.apps](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.apps)** contains the `/apps` and `/etc` parts of the project, i.e. JS and CSS clientlibs, components, and templates.
* **[ui.content](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.content)** contains sample content using the components from the ui.apps module.
* **[ui.config](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.config)** contains runmode-specific OSGi configs for the project.
* **[ui.frontend.general](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.general)** contains the artifacts required to use the general Webpack-based front-end build module (optional).
* **[ui.frontend.react](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.react)** **(optional)** contains the artifacts required when using the archetype to create a SPA projects based on React (optional, depends on build parameters).
* **[ui.frontend.angular](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.angular)** **(optional)** contains the artifacts required when using the archetype to create a SPA projects based on Angular (optional, depends on build parameters).
* **[ui.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** contains Selenium-based UI tests.
* **[all](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/all)** is a single content package that embeds all of the compiled modules (bundles and content packages) including any vendor dependencies.
* **[dispatcher.ams](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.ams)** contains the basic dispatcher configurations for AMS/on-prem projects(optional, depends on build parameters).
* **[dispatcher.cloud](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.cloud)** contains the basic dispatcher configurations for AEMaaCS projects (optional, depends on build parameters).

![Content package organization](/help/assets/content-package-organization.png)

The modules of the archetype represented in Maven are deployed to AEM as content packages representing the application, the content, and the necessary OSGi bundles.

## Parent POM {#parent-pom}

The `pom.xml` at the root of the project (`<src-directory>/<project>/pom.xml`) is known as the parent POM and drives the structure of the project as well as manages dependencies and certain global properties of the project.

### Global Project Properties {#global-properties}

The `<properties>` section of the parent POM defines several global properties that are important to the deployment of your project on an AEM instance such as user name/password, host name/port, etc.

These properties are set up to deploy to a local AEM instance, as this is the most common build that developers will do. Notice there are properties to deploy to an author instance as well as a publish instance. This is also where the credentials are set to authenticate with the AEM instance. The default `admin:admin` credentials are used.

These properties are set up so that they can be overridden when deploying to higher level environments. In this way the POM files do not have to change, but variables like `aem.host` and `sling.password` can be overridden via command line arguments:

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Module Structure {#module-structure}

The `<modules>` section of the parent POM defines the modules that the project will build. By default the project builds [the standard modules previously defined.](#what-you-get) More modules can always be added as a project evolves.

### Dependencies {#dependencies}

The `<dependencyManagement>` section of the parent POM defines all of the dependencies and versions of APIs that are used in the project. Versions should be managed in the parent POM. Sub-modules should not include any version information.

#### Uber-Jar {#uber-jar}

One of the key dependencies is the [AEM Java API Jar.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) This will include all of the AEM APIs with just a single dependency entry for the version of AEM.

>[!NOTE]
>
>As a best practice you should update the uber-jar version to match the target version of AEM. For example, if you plan to deploy to AEM 6.5 you should update the version of the uber-jar to 6.5.X, where `X` is the latest service pack.

#### Core Components {#core-components}

The archetype of course leverages the [Core Components.](/help/introduction.md) Therefore, in order to leverage the Core Components in all deployments, it is a best practice to include them as part of the Maven project.

The core.wcm.components.examples are a set of sample pages that illustrate examples of the Core Components. As a best practice, when deploying a project for production use you should remove this dependency and subpackage inclusion.

>[!NOTE]
>
>The Core Components and the archetype are maintained as separate GitHub projects and as such their releases differ.
>
>Each release of the archetype will utilize the latest release of the Core Components available at the time of the release. However, you may wish to update the dependency on the Core Components manually.

## Testing {#testing}

There are three levels of testing contained in the project and because they are different types of tests, they are executed in different ways or in different places.

* **[Unit Tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** - Classic unit testing of the code contained in the bundle
* **[Integration Tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** - Server-side integration tests that run unit-like tests in the AEM-environment, i.e. on the AEM server
* **[UI Tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** - Selenium-based browser-side tests that verify browser-side behavior
