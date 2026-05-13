---
title: Title Component
description: The Core Component Title Component is a section heading component that features in-place editing.
role: Developer, Admin, User
exl-id: 393af72c-549f-4609-afb0-2712f827b549
TQID: https://experienceleague.adobe.com/RXRZwYyw7Xpdf-N5JvS6-0uipl5HgFlzSSi5HMeSooc
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
    internal-label: Authoring
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Title Component{#title-component}

The Core Component Title Component is a section heading component that features in-place editing.

{{traditional-aem}}

## Usage {#usage}

The Title Component is intended to be used as the title or heading of a section of content. The available heading levels can be defined by the template author in the [design dialog](#design-dialog). The content editor can select from available headings levels in the [edit dialog](#edit-dialog). For added convenience, simple in-place editing of the heading text is also available.

## Version and Compatibility {#version-and-compatibility}

The current version of the Title Component is v3, which was introduced with release 2.18.0 of the Core Components in February 2022, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM 6.5 LTS|AEM as a Cloud Service|
|---|---|---|---|---|
|v3|-|Compatible|Compatible|Compatible|
|[v2](v2/title.md)|Compatible|Compatible|-|Compatible|
|[v1](v1/title-v1.md)|Compatible|Compatible|-|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Title Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_title).

### Technical Details {#technical-details}

The latest technical documentation about the Title Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_title_v3).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to define the title text as well as select the heading level.

* **Title** - If empty the page title will be used
* **Type / Size** - Defines the heading level of the title
* **Link** - Defines the content to which the title will link. This can be a path to a content page, an external URL, or a page anchor.
* **Open link in new tab** - When checked, the link will open in a new browser tab.
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

![Title Component's edit dialog](/help/assets/title-edit.png)

The in-place editor can also be used to edit the text of the title component.

![In-place editing of Title Component](/help/assets/title-edit-inline.png)

### Styles Tab {#styles-tab-edit}

The Title Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling).

Use the drop-down to select the styles that you want to apply to the component. Selections made in the edit dialog have the same effect as those chosen from the component toolbar.

Styles must be configured for this component in the [design dialog](#design-dialog) in order for the drop down menu to be available.

![Styles tab of the edit dialog of Title Component](/help/assets/title-edit-styles.png)

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the default heading level that title components will have when created by the content authors.

### Sizes Tab {#sizes-tab}

![Title Component's design dialog](/help/assets/title-design.png)

* **Allowed Types / Sizes for Authors** - Enable or disable heading types that will be available for content authors when they use the Title Component.
* **Default Type / Size**- Define the heading type that will be automatically assigned when a content author adds the Title Component to a page.
* **Disable Link**- Disable support for links in the title component to disallow content authors from linking from titles.

### Styles Tab {#styles-tab}

The Title Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

The Title Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
