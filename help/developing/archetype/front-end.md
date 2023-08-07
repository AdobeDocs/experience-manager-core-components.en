---
title: Front-End Development with the AEM Project Archetype
description: Learn about the AEM Project Archetype's optional, dedicated front-end build mechanism based on Webpack.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
---

# Front-End Development with the AEM Project Archetype {#front-end}

The AEM Project Archetype includes an optional, dedicated front-end build mechanism based on Webpack. The ui.frontend module thus becomes the central location for all of the project's front-end resources including JavaScript and CSS files. To fully take advantage of this useful and flexible feature, it is important to understand how front-end development fits into an AEM project.

This document focuses on general usage patterns of the front-end build module and what it does for you. For detailed build options and technical instructions, please see the documentation in the GitHub repository of the archetype.

>[!TIP]
>
>The latest AEM Project Archetype and associated technical documentation [can be found on GitHub.](https://github.com/adobe/aem-project-archetype)

## AEM Front-End and Back-End Development {#front-end-back-end}

In greatly-simplified terms, AEM projects can be thought of as consisting of two separate but related parts:

* Back-end development that drives the logic of AEM and produces Java libraries, OSGi services, etc.
* Front-end development that drives the presentation and behavior of the resulting web site and produces JavaScript and CSS libraries

Because these two development processes are focused on different parts of the project, back-end and front-end development can happen in parallel.

![front end workflow diagram](/help/assets/front-end-flow.png)

However, any resulting project needs to use the output of both of these development efforts i.e. both back-end and front-end.

## Determining the Markup {#determining-markup}

Whichever front-end development workflow you decide to implement for your project, the back-end developers and front-end developers must first agree on the markup. Typically AEM defines the markup, which is provided by the core components. [However this can be customized if necessary.](/help/developing/customizing.md#customizing-the-markup)

## Possible Front-End Development Workflows {#possible-workflows}

The front-end build module is a useful and very flexible tool, but imposes no particular opinion on how it should be used. The following are two examples of *possible* usage, but your individual project needs may dictate other use models.

### Using Webpack Static Development Server {#using-webpack}

Using Webpack you can style and develop based on static output of AEM webpages within the ui.frontend module.

1. Preview page in AEM using page preview mode or passing in `wcmmode=disabled` in the URL
1. View page source and save as static HTML within the ui.frontend module
1. [Start webpack](#webpack-dev-server) and begin styling and generating the necessary JavaScript and CSS
1. Run `npm run dev` to generate the clientlibs

In this flow, an AEM developer may perform steps one and two and pass the static HTML off to the front-end developer who develops based on the AEM HTML output.

>[!TIP]
>
>One could also leverage the [Component Library](https://adobe.com/go/aem_cmp_library) to capture samples of the markup output of each component in order to work at the component level rather than the page level.

### Using Storybook {#using-storybook}

Using [Storybook](https://storybook.js.org) you can perform more atomic front-end development. Although Storybook is not included in the AEM Project Archetype, you can install it and store your Storybook artifacts within the ui.frontend module. When ready for testing within AEM, they can be deployed as clientlibs by running `npm run dev`.

>[!NOTE]
>
>[Storybook](https://storybook.js.org) is not included in the AEM Project Archetype. If you choose to use it, you must install it separately.

## Clientlibs Overview {#clientlibs}

The frontend module is made available using an [AEM clientlib.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html). When executing the NPM build script, the app is built and the `aem-clientlib-generator` package takes the resulting build output and transforms it into such a clientlib.

A clientlib will consist of the following files and directories:

* `css/`: CSS files which can be requested in the HTML
* `css.txt`: Tells AEM the order and names of files in `css/` so they can be merged
* `js/`: JavaScript files which can be requested in the HTML
* `js.txt` Tells AEM the order and names of files in `js/` so they can be merged
* `resources/`: Source maps, non-entrypoint code chunks (resulting from code splitting), static assets (e.g. icons), etc.

>[!TIP]
>
>Learn more about how AEM handles clientlibs in the [AEM development documentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html) abd how to include them in the [Core Components documentation.](/help/developing/including-clientlibs.md)
