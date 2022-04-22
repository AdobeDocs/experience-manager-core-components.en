---
title: Table of Contents Component
description: The Table of Contents Component creates a ToC based on the titles in your page content allowing your readers to quickly navigate the page.
role: Architect, Developer, Admin, User
---
# Table of Contents Component {#table-of-contents-component}

The Table of Contents Component creates a ToC based on the titles in your page content allowing your readers to quickly navigate the page.

## Usage {#usage}

The Table of Contents component offers site visitors the ability to quickly navigate your page's content through a ToC generated based on the titles of the pages content.

The [edit dialog](#edit-dialog) allows the content author to define the range of titles to be used in the ToC. Using the [design dialog](#design-dialog), the template author can set the default value for the titles when a content author adds a Table of Contents Component to a page as well as restrict titles included in the ToC based on class names.

## Version and Compatibility {#version-and-compatibility}

The current version of the Table of Contents Component is v1, which was introduced with release 2.20.0 of the Core Components in May 2022, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.5|AEM as a Cloud Service|
|---|---|---|
|v1|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Table of Contents Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_tableofcontents).

### Technical Details {#technical-details}

The latest technical documentation about the Table of Contents Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to define the ranges of title levels that the Table of Contents Component should render as a ToC.

![Table of Contents Component's edit dialog](/help/assets/tableofcontents-edit.png)

**List Type** - This option defines if the list should be a bulleted list or a numbered list.
* **Title Start Level** - This option defines the highest level of titles that the Table of Contents Component should render.
* **Title Stop Level** - This option defines the lowest level of titles that the Table of Contents Component should render.
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Design Dialog {#design-dialog}

Using the design dialog, the template author can set the default value for the title range of the Table of Contents Component as well as restrict titles included in the ToC based on class names.

### Properties Tab {#properties-tab}

![Quick Search Component's design dialog](/help/assets/tableofcontents-design.png)

* **Restrict List Type** - This option defines the type of list that the component will generate. Selecting this option restricts the content author's ability to choose a different list type.
* **Restrict the Start Level** - This option defines the highest title level that the content author can select for defining the ToC.
* **Restrict the Stop Level** - This option defines the lowest title level that the content author can select for defining the ToC.
* **Include Class Names** - If this option is set, only titles with the specified class names or contained within elements of the specified class names will be considered by the Table of Contents Component.
  * Tap or click the **Add** icon to add one or more class names.
  * Tap or click the **Delete** icon next to a class name to delete it.
* **Ignore Class Names** - If this option is set, titles with the specified class names or contained within elements of the specified class names will be ignored by the Table of Contents Component.
  * Tap or click the **Add** icon to add one or more class names.
  * Tap or click the **Delete** icon next to a class name to delete it.

### Styles Tab {#styles-tab}

The Table of Contents Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

The Table of Contents Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
