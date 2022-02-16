---
title: Breadcrumb Component (v2)
description: The Core Component Breadcrumb Component is a navigation component that builds a breadcrumb of links based on the page's location in the content hierarchy.
role: Architect, Developer, Admin, User
exl-id: 5f2e6fef-e2f6-48e2-8dac-008db3131044
---
# Breadcrumb Component (v2) {#breadcrumb-component}

The Core Component Breadcrumb Component is a navigation component that builds a breadcrumb of links based on the page's location in the content hierarchy.

## Usage {#usage}

The Breadcrumb Component displays the position of the current page within the site hierarchy, allowing page visitors to navigate the page hierarchy from their current location. This is often integrated into page headers or footers.

Available options, such as the default navigation level and the ability to show the current page or hidden pages, can be defined by the template author in the [design dialog](#design-dialog). The content editor can then choose if hidden pages should be shown or not and the actual navigation level for the component in the [edit dialog](#edit-dialog).

## Version and Compatibility {#version-and-compatibility}

This document describes v2 of the Breadcrumb Component, which was introduced with release 2.0.0 of the Core Components in January 2018.

>[!CAUTION]
>
>This document describes v2 of the Breadcrumb Component.
>
>For details of the current version of the Breadcrumb Component, see the [Breadcrumb Component](/help/components/breadcrumb.md) document.

## Sample Component Output {#sample-component-output}

To experience the Breadcrumb Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_breadcrumb).

>[!NOTE]
>
>As of Core Components release 2.1.0, the Breadcrumb Component supports [schema.org microdata](https://schema.org/BreadcrumbList).

## Technical Details {#technical-details}

The latest technical documentation about the Breadcrumb Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to suppress hidden and active pages in the breadcrumbs as well as the depth in the hierarchy it should display.

![Breadcrumb component edit dialog](/help/assets/breadcrumb-edit.png)

* **Navigation Start Level** - Where in the hierarchy the breadcrumb component should start to walk down to the current page. For example:

    * 0 starts at `/content`  
    * 1 starts at `/content/<yourSite>`
    * 2 starts at `/content/<yourSite>/<country>`

* **Show hidden navigation items** - Show pages marked as hidden in the breadcrumb (by default they will not be displayed)
* **Hide current page** - Suppress the current page in the breadcrumb (by default it will be displayed)
* **Disable shadowing** - If the page in the hierarchy is a redirect, the name of the redirecting page will be shown instead of the target. See the [Shadow Site Structure Support](../v1/navigation.md#shadow-structure) of the Navigation Component for more information.
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define what the default values are for the options to suppress hidden and active pages in the breadcrumbs as well as the depth in the hierarchy it should display.

### Main Tab {#main-tab}

![](/help/assets/breadcrumb-design.png)

* **Navigation Start Level** - Defines the default value for where in the hierarchy the breadcrumb component should start to walk down to the current page when the breadcrumb component is added to a page.
* **Show hidden navigation items** - Defines the default value of the **Show hidden navigation items** option when the breadcrumb component is added to a page.

    * It does not enable or disable the option for the author. It only sets the default value.

* **Hide current page**- Defines the default value of the **Hide current page** option when the breadcrumb component is added to a page.

    * It does not enable or disable the option for the author. It only sets the default value.

* **Disable shadowing** - Defines the default value of the **Disable shadowing** option when the breadcrumb component is added to a page.

### Styles Tab {#styles-tab}

The Breadcrumb Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

The Breadcrumb Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
