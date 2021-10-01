---
title: Using the AEM Project Archetype
description: Detailed usage instructions for the AEM Project Archetype
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
---
# AEM Project Archetype {#aem-project-archetype}

The AEM Project Archetype creates a minimal, best-practices-based Adobe Experience Manager project as a starting point for your own AEM projects. The properties that must be provided when using this archetype allow you to specify the names for all parts of this project as well as control certain optional features.

## Why Use the Archetype {#why-use-the-archetype}

Using the AEM Project Archetype sets you on the path towards building a best-practices-based AEM project with just a few keystrokes. By using the archetype, all of the pieces will already in place so that while the resulting project is minimal, it already implements all of the [key features](#what-you-get) of AEM so that all you have to do is build on top and extend.

Of course there are many elements that go into a successful AEM project, but using the AEM Project Archetype is a sound foundation and is strongly recommended for any AEM project.

## Getting Started {#getting-started}

The project archetype makes it easy to get started developing on AEM. You can take your first steps in a number of ways.

* WKND Tutorial - For a great introduction to developing on AEM including how to leverage the archetype see the [Getting Started with AEM Sites - WKND Tutorial](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) for a practical example that walks you through using the archetype to implement a simple project.
* WKND Events Tutorial - If you are particularly interested in single page application (SPA) development on AEM, be sure to check out dedicated [WKND Events tutorial](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html).
* Download and start on your own! - You can easily download the current project archetype available on GitHub and create your first project by [following the simple steps below](#how-to-use-the-archetype).

## What You Get Using the Archetype {#what-you-get}

The AEM Archetype is made up of modules:

* **[core](core.md)**: is a Java bundle containing all core functionality like OSGi services, listeners, and schedulers, as well as component-related Java code such as servlets and request filters.
* **[it.tests](ittests.md)**: are Java-based integration tests.
* **[ui.apps](uiapps.md)**: contains the `/apps` and `/etc` parts of the project, i.e. JS and CSS clientlibs, components, and templates.
* **[ui.content](uicontent.md)**: contains sample content using the components from the ui.apps module.
* **ui.config**: contains runmode-specific OSGi configs for the project.
* **[ui.frontend.general](uifrontend.md)**: **(optional)** contains the artifacts required to use the general Webpack-based front-end build module.
* **[ui.frontend.react](uifrontend-react.md)**: **(optional)** contains the artifacts required when using the archetype to create a SPA projects based on React.
* **[ui.frontend.angular](uifrontend-angular.md)**: **(optional)** contains the artifacts required when using the archetype to create a SPA projects based on Angular.
* **[ui.tests](uitests.md)**: contains Selenium-based UI tests.
* **all**: is a single content package that embeds all of the compiled modules (bundles and content packages) including any vendor dependencies.
* **analyse**: runs analysis on the project, which provides additional validation for deploying into AEM as a Cloud Service.

![](/help/assets/archetype-structure.png)

The modules of AEM Archetype represented in Maven are deployed to AEM as content packages representing the application, the content, and the necessary OSGi bundles.

## How to Use the Archetype {#how-to-use-the-archetype}

To use the archetype, you first need to create a project, which generates the modules in a local file structure as [previously described](#what-you-get). As part of project generation, a number of properties for your project can be defined such as project name, version, etc.

Building the project with Maven creates the artifacts (packages and OSGi bundles), that can be deployed to AEM. Additional Maven commands and profiles can be used to deploy the project artifacts to an AEM instance.

### Creating a Project {#create-project}

To get started you can most simply use the [AEM Eclipse extension](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/eclipse.html) and follow the New Project wizard and choosing **AEM Sample Multi-Module Project** to use a released version of the archetype.

Of course you can also invoke Maven directly.

```shell
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Set `XX` to the [version number](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) of the latest AEM Project Archetype.
* Set `aemVersion=cloud` for [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html);  
 Set `aemVersion=6.5.0` for [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams), or on-premise.
 The Core Components dependency is only added for non cloud aem versions as the Core Components are provided OOTB for AEM as a Cloud 
 Service.
* Adjust `appTitle="My Site"` to define the website title and components groups.
* Adjust `appId="mysite"` to define the Maven artifactId, the component, config and content folder names, as well as client library names.
* Adjust `groupId="com.mysite"` to define the Maven groupId and the Java Source Package.
* Lookup the list of available properties to see if there's more you want to adjust.

>[!NOTE]
>
>It is best practice to add the `adobe-public` profile to your Maven `settings.xml` file in order to automatically add repo.adobe.com to the maven build process.
>
>An example POM [can be found here](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

### Properties {#properties}

The following properties are available when creating a project using the archetype.

| Name                      | Default        | Description        |
|---------------------------|----------------|--------------------|
| `appTitle`                |                | Application title, will be used for website title and components groups (e.g. `"My Site"`). |
| `appId`                   |                | Technical name, will be used for component, config and content folder names, as well as client library names (e.g. `"mysite"`). |
| `artifactId`              | *`${appId}`*   | Base Maven artifact ID (e.g. `"mysite"`). |
| `groupId`                 |                | Base Maven group ID (e.g. `"com.mysite"`). |
| `package`                 | *`${groupId}`* | Java Source Package (e.g. `"com.mysite"`). |
| `version`                 | `1.0-SNAPSHOT` | Project version (e.g. `1.0-SNAPSHOT`). |
| `aemVersion`              | `cloud`        | Target AEM version (can be `cloud` for [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html); or `6.5.0`, or `6.4.4` for [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) or on-premise). |
| `sdkVersion`              | `latest`       | When `aemVersion=cloud` an [SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) version can be specified (e.g. `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y`            | Includes a dispatcher configuration either for cloud or for AMS/on-premise, depending of the value of `aemVersion` (can be `y` or `n`). |
| `frontendModule`          | `general`      | Includes a Webpack frontend build module that generates the client libraries (can be `general` or `none` for regular sites; can be `angular` or `react` for a Single Page App that implements the [SPA Editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html)). |
| `language`                | `en`           | Language code (ISO 639-1) to create the content structure from (e.g. `en`, `deu`). |
| `country`                 | `us`           | Country code (ISO 3166-1) to create the content structure from (e.g. `US`). |
| `singleCountry`           | `y`            | Includes a language-master content structure (can be `y`, or `n`). |
| `includeExamples`         | `n`            | Includes a [Component Library](https://www.aemcomponents.dev/) example site (can be `y`, or `n`). |
| `includeErrorHandler`     | `n`            | Includes a custom 404 response page that will be global to the entire instance (can be `y` or `n`). |
| `includeCommerce`         | `n`            | Includes [CIF Core Components](https://github.com/adobe/aem-core-cif-components) dependencies and generates corresponding artifacts. |
| `commerceEndpoint`        |                | Required for CIF only. Optional endpoint of the commerce system GraphQL service to be used (e.g. `https://hostname.com/grapql`). |
| `datalayer`               | `y`            | Activate integration with [Adobe Client Data Layer](/help/developing/data-layer/overview.md). |
| `amp`                     | `n`            | Enable [AMP](/help/developing/amp.md) support for generated project templates. |
| `enableDynamicMedia`      | `n`            | Enables foundation DynamicMedia components in project policy settings and activates Dynamic Media features in Core Image component's policy. |
| `enableSSR`               | `n`            | Option to enable SSR for the front-end project |
| `precompiledScripts`      | `n`            | Option to [precompile](/help/developing/archetype/precompiled-bundled-scripts.md) the server-side scripts from `ui.apps` and attach them to the build as a secondary bundle artifact in the `ui.apps` project. `aemVersion` should be set to `cloud`. |

>[!NOTE]
>
> If the archetype is executed in interactive mode the first time, properties with default values can't be changed (see [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) for more details). The value can be changed when the property confirmation at the end is denied and the questionnaire gets repeated, or by passing the parameter in the command line (e.g. `-DoptionIncludeExamples=n`).

>[!NOTE]
>
>When running on Windows and generating the dispatcher configuration, you should be running in an elevated command prompt or the Windows Subsystem for Linux (see [issue 329](https://github.com/adobe/aem-project-archetype/issues/329)).

### Profiles {#profiles}

The generated maven project supports different deployment profiles when running `mvn install`.

| Profile ID                        | Description |
| --------------------------|------------------------------|
| `autoInstallBundle`         | Install core bundle with the maven-sling-plugin to the felix console |
| `autoInstallPackage`        | Install the ui.content and ui.apps content package with the content-package-maven-plugin to the package manager to default author instance on localhost, port 4502. Hostname and port can be changed with the `aem.host` and `aem.port` user defined properties. |
| `autoInstallPackagePublish` | Install the ui.content and ui.apps content package with the content-package-maven-plugin to the package manager to default publish instance on localhost, port 4503. Hostname and port can be changed with the `aem.host` and `aem.port` user defined properties. |
| `autoInstallSinglePackage`  | Install the `all` content package with the content-package-maven-plugin to the package manager to default author instance on localhost, port 4502. Hostname and port can be changed with the `aem.host` and `aem.port` user defined properties. |
| `autoInstallSinglePackagePublish` |  Install the `all` content package with the content-package-maven-plugin to the package manager to default publish instance on localhost, port 4503. Hostname and port can be changed with the `aem.host` and `aem.port` user defined properties. |
| `integrationTests` | Runs the provided integration tests on the AEM instance (only for the `verify` phase) |
| `precompiledScripts` | Defined automatically when the project was generated with the `precompiledScripts` property set to `y`. The profile is active by default and generates an OSGi bundle inside `ui.apps` with the precompiled scripts, which will be included in the `all` content package. The profile can be disabled with `-DskipScriptPrecompilation=true`. |

### Building and Installing {#building-and-installing}

To build all the modules run in the project root directory, use the following Maven command.

```shell
mvn clean install
```

If you have a running AEM instance, you can build and package the whole project and deploy into AEM with the following Maven command.

```shell
mvn clean install -PautoInstallPackage
```

To deploy it to a publish instance, run this command.

```shell
mvn clean install -PautoInstallPackagePublish
```

Alternatively, to deploy to a publish instance, run this command.

```shell
mvn clean install -PautoInstallPackage -Daem.port=4503
```

Or to deploy only the bundle to the author, run this command.

```shell
mvn clean install -PautoInstallBundle
```

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

The `<modules>` section of the parent POM defines the modules that the project will build. By default the project builds [the standard modules previously defined](#what-you-get): core, ui.apps, ui.content, ui.tests, and it.launcher. More modules can always be added as a project evolves.

### Dependencies {#dependencies}

The `<dependencyManagement>` section of the parent POM defines all of the dependencies and versions of APIs that are used in the project. Versions should be managed in the Parent POM. Sub-modules like core and ui.apps should not include any version information.

#### Uber-Jar {#uber-jar}

One of the key dependencies is the [AEM Java API Jar](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html). This will include all of the AEM APIs with just a single dependency entry for the version of AEM.

>[!NOTE]
>
>As a best practice you should update the uber-jar version to match the target version of AEM. For example, if you plan to deploy to AEM 6.4 you should update the version of the uber-jar to 6.4.0.

#### Core Components {#core-components}

The AEM Project Archetype of course leverages the Core Components.

The Core Components are installed in AEM automatically in the default runmode and used by the sample WKND site. In a [production runmode](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#runmodes) (`nosamplecontent`) the Core Components are not available.

Therefore, in order to leverage the Core Components in all deployments, it is a best practice to include them as part of the Maven project.

>[!NOTE]
>
>Each release of the Core Components is generally followed by a release of the AEM Project Archetype so that the latest archetype uses the latest version of the core components.
>
>However a new version of the archetype may not directly follow a new version of the Core Components, so you may wish to update the dependency on the Core Components to the latest version.

>[!NOTE]
>
>The core.wcm.components.examples are a set of sample pages that illustrate examples of the Core Components. As a best practice, when deploying a project for production use you should remove this dependency and subpackage inclusion.

## Testing {#testing}

There are three levels of testing contained in the project and because they are different types of tests, they are executed in different ways or in different places.

* Unit test in core: This showcases classic unit testing of the code contained in the bundle. To test, execute:
  * `mvn clean test`
* Server-side integration tests: These run unit-like tests in the AEM-environment, i.e. on the AEM server. To test, execute:
  * `mvn clean verify -PintegrationTests`
* Client-side Hobbes.js tests: These are JavaScript-based browser-side tests that verify browser-side behavior. To test:
  1. Load AEM in your browser as you would to author a page.
  1. Open the page in [Developer mode](https://experienceleague.adobe.com/docs/experience-manager-65/developing/components/developer-mode.html)
  1. Open the left panel and switch to the **Tests** tab.
  1. Find the generated **MyName Tests** and run them.

## Next Steps {#next-steps}

So you have built and installed the AEM Project Archetype. What now? Well, the archetype is small, but consists of many examples of powerful AEM features configured according to recommended best practices. Use these are indicatory of how you can leverage these features in your project. For any project you likely need to:

* [Customize components by extending the existing core components](/help/developing/customizing.md)
* [Add additional templates](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [Adapt the localization structure](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/preparation.html)
* [Learn about the front-end build module](uifrontend.md)
