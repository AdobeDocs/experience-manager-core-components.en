---
title: Using the AEM Project Archetype
description: Detailed usage instructions for the AEM Project Archetype
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
---

# Using the AEM Project Archetype {#using-the-archetype}

The AEM Project Archetype creates a minimal, best-practices-based Adobe Experience Manager project as a starting point for your own AEM projects.

>[!TIP]
>
>The latest AEM Project Archetype and associated technical documentation [can be found on GitHub.](https://github.com/adobe/aem-project-archetype)

## Getting Started {#getting-started}

The project archetype makes it easy to get started developing on AEM. You can take your first steps in a number of ways.

* WKND Tutorial - For a great introduction to developing on AEM including how to leverage the archetype see the [Getting Started with AEM Sites - WKND Tutorial](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) for a practical example that walks you through using the archetype to implement a simple project.
* WKND Events Tutorial - If you are particularly interested in single page application (SPA) development on AEM, be sure to check out dedicated [WKND Events tutorial](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html).
* Download and start on your own! - You can easily download the [current project archetype available on GitHub](https://github.com/adobe/aem-project-archetype) and create your first project.

## How to Use the Archetype {#how-to-use-the-archetype}

To use the archetype, you first need to create a project, which generates the modules in a local file structure as [previously described](#what-you-get). As part of project generation, a number of properties for your project can be defined such as project name, version, etc.

You can choose to create your project by following one of the [previously-listed options.](#getting-started)

Building the project with Maven creates the artifacts (packages and OSGi bundles), that can be deployed to AEM. Additional Maven commands and profiles can be used to deploy the project artifacts to an AEM instance.

## What You Get Using the Archetype {#what-you-get}

The AEM Archetype is made up of modules, all of which are created automatically when using the archetype.

* **[core](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)**: is a Java bundle containing all core functionality like OSGi services, listeners, and schedulers, as well as component-related Java code such as servlets and request filters.
* **[it.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)**: are Java-based integration tests.
* **[ui.apps](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.apps)**: contains the `/apps` and `/etc` parts of the project, i.e. JS and CSS clientlibs, components, and templates.
* **[ui.content](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.content)**: contains sample content using the components from the ui.apps module.
* **ui.config**: contains runmode-specific OSGi configs for the project.
* **[ui.frontend.general](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.general)**: **(optional)** contains the artifacts required to use the general Webpack-based front-end build module.
* **[ui.frontend.react](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.react)**: **(optional)** contains the artifacts required when using the archetype to create a SPA projects based on React.
* **[ui.frontend.angular](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.angular)**: **(optional)** contains the artifacts required when using the archetype to create a SPA projects based on Angular.
* **[ui.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)**: contains Selenium-based UI tests.
* **[all](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/all)**: is a single content package that embeds all of the compiled modules (bundles and content packages) including any vendor dependencies.
* **[dispatcher.ams](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.ams)**: Contains the basic dispatcher configurations for AMS/on-prem projects
* **[dispatcher.cloud](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.cloud)**: This module contains the basic dispatcher configurations for AEMaaCS projects

![Content package organization](/help/assets/content-package-organization.png)

The modules of AEM Archetype represented in Maven are deployed to AEM as content packages representing the application, the content, and the necessary OSGi bundles.

## Parent POM {#parent-pom}

The `pom.xml` at the root of the project (`<src-directory>/<project>/pom.xml`) is known as the parent POM and drives the structure of the project as well as manages dependencies and certain global properties of the project.

### Global Project Properties {#global-properties}

The `<properties>` section of the parent POM defines several global properties that are important to the deployment of your project on an AEM instance such as user name/password, host name/port, etc.

These properties are set up to deploy to a local AEM instance, as this is the most common build that developers will do. Notice there are properties to deploy to an author instance as well as a publish instance. This is also where the credentials are set to authenticate with the AEM instance. The default admin:admin credentials are used.

These properties are set up so that they can be overridden when deploying to higher level environments. In this way the POM files do not have to change, but variables like `aem.host` and `sling.password` can be overridden via command line arguments:

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Module Structure {#module-structure}

The `<modules>` section of the parent POM defines the modules that the project will build. By default the project builds [the standard modules previously defined.](#what-you-get) More modules can always be added as a project evolves.

### Dependencies {#dependencies}

The `<dependencyManagement>` section of the parent POM defines all of the dependencies and versions of APIs that are used in the project. Versions should be managed in the Parent POM. Sub-modules should not include any version information.

#### Uber-Jar {#uber-jar}

One of the key dependencies is the [AEM Java API Jar](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html). This will include all of the AEM APIs with just a single dependency entry for the version of AEM.

>[!NOTE]
>
>As a best practice you should update the uber-jar version to match the target version of AEM. For example, if you plan to deploy to AEM 6.5 you should update the version of the uber-jar to 6.5.X, where `X` is the latest service pack.

#### Core Components {#core-components}

The AEM Project Archetype of course leverages the Core Components. Therefore, in order to leverage the Core Components in all deployments, it is a best practice to include them as part of the Maven project.

The core.wcm.components.examples are a set of sample pages that illustrate examples of the Core Components. As a best practice, when deploying a project for production use you should remove this dependency and subpackage inclusion.

>[!NOTE]
>
>The Core Components and the archetype are maintained as separate GitHub projects and as such their releases differ.
>
>Each release of the archetype will utilize the latest release of the Core Components. However, a new version of the archetype may not directly follow a new version of the Core Components, so you may wish to update the dependency on the Core Components to the latest version proactively.

## Testing {#testing}

There are three levels of testing contained in the project and because they are different types of tests, they are executed in different ways or in different places.

* [Unit Tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core) - Classic unit testing of the code contained in the bundle
* [Integration Tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests) - Server-side integration tests that run unit-like tests in the AEM-environment, i.e. on the AEM server
* [UI Tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests) - JavaScript-based browser-side tests that verify browser-side behavior
