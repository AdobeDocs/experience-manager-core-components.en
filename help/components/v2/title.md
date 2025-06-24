---
title: Title Component (v2)
description: The Core Component Title Component is a section heading component that features in-place editing.
role: Architect, Developer, Admin, User
exl-id: f853ec46-19fd-4569-a9d3-5c376d2a2101
index: n
---

# Title Component (v2) {#title-component}

The Core Component Title Component is a section heading component that features in-place editing.

## Usage {#usage}

The Title Component is intended to be used as the title or heading of a section of content. The available heading levels can be defined by the template author in the [design dialog](#design-dialog). The content editor can select from available headings levels in the [edit dialog](#edit-dialog). For added convenience, simple in-place editing of the heading text is also available.

## Version and Compatibility {#version-and-compatibility}

This document describes v2 of the Title Component, which was introduced with release 2.0.0 of the Core Components in January 2018.

>[!CAUTION]
>
>This document describes v2 of the Title Component.
>
>For details of the current version of the Title Component, see the [Title Component](/help/components/title.md) document.

## Sample Component Output {#sample-component-output}

To experience the Title Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_title).

### Technical Details {#technical-details}

The latest technical documentation about the Title Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_title_v2).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to define the title text as well as select the heading level.

* **Title** - If empty the page title will be used
* **Type / Size** - Defines the heading level of the title
* **Link** - Defines the content to which the title will link. This can be a path to a content page, an external URL, or a page anchor.
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

![Title Component's edit dialog](/help/assets/title-edit.png)

>[!NOTE]
>
>The ability to define a link for the title was introduced with release 2.2.0 of the Core Components.

The in-place editor can also be used to edit the text of the title component.

![In-place editing of Title Component](/help/assets/title-edit-inline.png)

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the default heading level that title components will have when created by the content authors.

### Sizes Tab {#sizes-tab}

![Title Component's design dialog](/help/assets/title-design.png)

* **Allowed Types / Sizes for Authors** - Enable or disable heading types that will be available for content authors when they use the Title Component.
* **Default Type / Size**- Define the heading type that will be automatically assigned when a content author adds the Title Component to a page.
* **Disable Link**- Disable support for links in the title component to disallow content authors from linking from titles.

>[!NOTE]
>
>The ability to define a link for the title was introduced with release 2.2.0 of the Core Components.

### Styles Tab {#styles-tab}

The Title Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

The Title Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
