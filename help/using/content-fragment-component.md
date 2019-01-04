---
title: Content Fragment Component
seo-title: Content Fragment Component
description: null
seo-description: The Core Component Content Fragment component allows for the display of a content fragment.
uuid: ec807de9-f76c-4850-9ece-c3e439a1d626
contentOwner: User
content-type: reference
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: f093f58e-9755-4a4f-803a-ab93a50e6870
---

# Content Fragment Component{#content-fragment-component}

The Core Component Content Fragment component allows for the display of a [content fragment](https://helpx.adobe.com/experience-manager/6-4/assets/using/content-fragments.html).

>[!NOTE]
>
>The Core Component Content Fragment component requires release 1.1.0 or higher of the core components. Please see the [compatiblity information for Core Components v1](versions.md#main-pars_title_236368006) for more information.

>[!NOTE]
>
>For compatibility reasons, the Core Component Content Fragment component was made available with release 1.1.0 as an extension to the core components and therefore must be separately downloaded and explicitly enabled. 
>
>In release 1.1.0, the Content Fragment component was in the sandbox branch, meaning that this was a pre-release technology preview and was not recommended for production.

## Usage {#usage}

The Core Component Content Fragment Component allows for the inclusion of a [content fragment](https://helpx.adobe.com/experience-manager/6-4/assets/using/content-fragments.html) on a page.

* The fragment and its properties can be selected in the [configure dialog](content-fragment-component.md#main-pars_title_1002684262).
* Resource types to handle certain images and grids can be defined in the [design dialog](#contentbody_title_277392253).
* The edit option will open the selected fragment within the [content fragment editor](https://helpx.adobe.com/experience-manager/6-4/assets/using/content-fragments-editor.html).

## Version and Compatibility {#version-and-compatibility}

The current version of the Content Fragment Component is v1, which was introduced with release 1.1.0 of the Core Components in October 2017, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.3|AEM 6.4|
|--- |--- |--- |
|v1|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

The following is sample taken from [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

## HTML {#html}

```
<div class="contentfragment aem-GridColumn aem-GridColumn--default--12">
    <div data-path="/content/dam/we-retail/our-favorite-toast" class="cmp-contentfragment">
        <div>
<div class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
</div></div>
        <div>
            <p>It is a difficult thing to try and describe the perfect toast.</p>
            <div>
<div class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
</div></div>
        </div>
    </div>
</div>
```

### JSON {#json}

```
 "contentfragment": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "dam/cfm/components/contentfragment",
              "text": "",
              "fileReference": "/content/dam/we-retail/en/products/activities/our-favorite-toast",
              "variation": "master",
              "element": "toastType"
            }
```

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the which content fragment and the elements of that fragment to be included.

![](assets/chlimage_1-87.png)

* **Content Fragment**

  * Path to the desired content fragment
  * The **Selection Dialog** can be used to locate the fragment

* **Element** - The element of the content fragment to include
* **Variation** - Which variation of the content fragment to use (defaults to **Master**)

* **Paragraphs**

  * **All** - Display all paragraphs
  * **Range**

    * Specify ranges of paragraphs which should be displayed, separated by a semicolon
    * For instance `1;3-5;7;9-*` to include the 1st, the 3rd to 5th, the 7th, and the 9th to the final paragraphs

* **Handle heading as their own paragraphs**

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the resource types used to handle mixed-media images and responsive grids.

![](assets/chlimage_1-88.png)

* **Mixed-media image type**

  * A Sling resource type that is used for rendering mixed-media images

* **Internal responsive grid**

  * The Sling resource type that is used for the internal responsive grid

## Technical Details {#technical-details}

The latest technical documentation about the Content Fragment Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragment/v1/contentfragment).

The entire core components project can be downloaded from GitHub.

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md). 
