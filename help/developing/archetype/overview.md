---
title: AEM Project Archetype
description: A project template for AEM-based applications
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
---
# AEM Project Archetype {#aem-project-archetype}

The AEM Project Archetype is a Maven template that creates a minimal, best-practices-based Adobe Experience Manager (AEM) project as a starting point for your website.

>[!TIP]
>
>The latest AEM Project Archetype [can be found on GitHub.](https://github.com/adobe/aem-project-archetype)

## Resources {#resources}

* **Archetype Documentation (this document):** Overview of the archetype architecture and its different modules.
  * **[Using the Archetype:](using.md)** further details on using the archetype and the modules available
  * **[ui.frontend:](uifrontend.md)** How to use the front end build module
* The following tutorials are based off this archetype:
  * **[WKND Site:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** Learn how to start a fresh new website.
  * **[WKND Single Page App:](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** Learn how to build a React or Angular webapp that is fully authorable in AEM.

## Features {#features}

* **Best Practice:** Bootstrap your site with all of Adobe's latest recommended practices.
* **Low-Code:** Edit your templates, create content, deploy your CSS, and your site is ready for go-live.
* **Cloud-Ready:** If desired, use [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) to go-live in few days and ease scalability and maintenance.
* **Dispatcher:** A project is complete only with a [Dispatcher configuration](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/dispatcher.html) that ensures speed and security.
* **Multi-Site:** If needed, the archetype generates the content structure for a [multi-language and multi-region setup](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html).
* **Core Components:** Authors can create nearly any layout with our versatile [set of standardized components](/help/introduction.md).
* **Editable Templates:** Assemble virtually any [template without code](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html), and define what the authors are allowed to edit.
* **Responsive Layout:** On templates or individual pages, [define how the elements reflow](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html) for the defined breakpoints.
* **Header and Footer:** Assemble and localize them without code, using the [localization features of the components](https://docs.adobe.com/content/help/en/experience-manager-core-components/using/get-started/localization.html).
* **Style System:** Avoid building custom components by allowing authors to [apply different styles](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) to them.
* **Front-End Build:** Front-end developers can [mock AEM pages](uifrontend.md#webpack-dev-server) and [build client libraries](uifrontend.md) with Webpack, TypeScript, and SASS.
* **WebApp-Ready:** For sites using [React](uifrontend-react.md) or [Angular](uifrontend-angular.md), use the [SPA SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/developing.html) to retain [in-context authoring of the app](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html).
* **Commerce Enabled:** For projects that want to integrate [AEM Commerce](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/commerce/home.html) with commerce solutions like [Magento](https://magento.com/) using the [Commerce Core Components](https://github.com/adobe/aem-core-cif-components).
* **Example Code:** Checkout the HelloWorld component, and the sample models, servlets, filters, and schedulers.
* **Open Sourced:** If something is not as it should, [contribute](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) your improvements!

## Usage {#usage}

To generate a project, adjust the following command line to your needs:

```shell
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
```

* Replace `XX` with the latest [archetype version number.](#requirements)
* Set `aemVersion=cloud` for [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);  
 Set `aemVersion=6.5.0` for [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams), or on-premise.
 The Core Components dependency is only added for non cloud aem versions as the Core Components are provided OOTB for AEM as a Cloud Service.
* Adjust `appTitle="My Site"` to define the website title and components groups.
* Adjust `appId="mysite"` to define the Maven artifactId, the component, config and content folder names, as well as client library names.
* Adjust `groupId="com.mysite"` to define the Maven groupId and the Java Source Package.
* Lookup the list of available properties to see if there's more you want to adjust.

## Available Properties {#available-properties}

| Name                      | Default        | Description        |
|---------------------------|----------------|--------------------|
| `appTitle`                |                | Application title, will be used for website title and components groups (e.g. `"My Site"`). |
| `appId`                   |                | Technical name, will be used for component, config and content folder names, as well as client library names (e.g. `"mysite"`). |
| `artifactId`              | *`${appId}`*   | Base Maven artifact ID (e.g. `"mysite"`). |
| `groupId`                 |                | Base Maven group ID (e.g. `"com.mysite"`). |
| `package`                 | *`${groupId}`* | Java Source Package (e.g. `"com.mysite"`). |
| `version`                 | `1.0-SNAPSHOT` | Project version (e.g. `1.0-SNAPSHOT`). |
| `aemVersion`              | `cloud`        | Target AEM version (can be `cloud` for [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html); or `6.5.0`, or `6.4.4` for [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) or on-premise). |
| `sdkVersion`              | `latest`       | When `aemVersion=cloud` an [SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) version can be specified (e.g. `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y`            | Includes a dispatcher configuration either for cloud or for AMS/on-premise, depending of the value of `aemVersion` (can be `y` or `n`). |
| `frontendModule`          | `general`      | Includes a Webpack frontend build module that generates the client libraries (can be `general` or `none` for regular sites; can be `angular` or `react` for a Single Page App that implements the [SPA Editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html)). |
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

## System Requirements {#requirements}

|Archetype | AEM as a Cloud Service | AEM 6.5 | Java SE | Maven|
|---------|---------|---------|---------|---------|
|[30](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-30) | Continual | 6.5.7.0+ | 8, 11 | 3.3.9+|

Setup your local development environment for [AEM as a Cloud Service SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) or for [older versions of AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

### Known Issues {#known-issues}

When running on Windows and generating the dispatcher configuration, you should be running in an elevated command prompt or the Windows Subsystem for Linux (see [#329](https://github.com/adobe/aem-project-archetype/issues/329)).

When executing the archetype in interactive mode (without the `-B` parameter), the properties with default values cannot be changed, unless the final confirmation gets dismissed, which then repeats the questions by including the properties with default values in the questions (see
[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) for details).

You can't use this archetype in Eclipse when starting a new project with `File -> New -> Maven Project` since the post generation script `archetype-post-generate.groovy` will not be executed due to an [Eclipse issue.](https://bugs.eclipse.org/bugs/show_bug.cgi?id=514993) The workaround is to use the above command line and then in Eclipse use `File -> Import -> Existing Maven Project`.

## Further Reading {#further-reading}

For more details on using the archetype including its benefits, options, and how its modules work, please see the [Using the Archetype document.](using.md)
