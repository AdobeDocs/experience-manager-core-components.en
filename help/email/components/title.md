---
title: Email Title Component
description: The Email Title Component is a section heading component for your emails that features in-place editing.
role: Architect, Developer, Admin, User
hidefromtoc: yes
index: no
---

# Email Title Component {#email-title-component}

The Email Title Component is a section heading component for your emails that features in-place editing.

## Usage {#usage}

The Email Title Component is intended to be used as the title or heading of a section of an email.

* The available heading levels can be defined by the template author in the [design dialog.](#design-dialog)
* The content author can select from available headings levels in the [edit dialog.](#edit-dialog)

For added convenience, simple in-place editing of the heading text is also available.

## Version and Compatibility {#version-and-compatibility}

The current version of the Email Title Component is v1, which was introduced with release x of the Email Core Components in October 2022, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.5|AEM as a Cloud Service|
|---|---|---|
|v1|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Email Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Title Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library.](https://adobe.com/go/aem_cmp_library_email_title)

### Technical Details {#technical-details}

The latest technical documentation about the Title Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_email_title_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to define the title text as well as select the heading level.

* **Title** - If empty the page title will be used
  * Click the Campaign icon to open the [Select Adobe Campaign Variable](/help/email/campaign-variables.md) dialog to insert dynamic content from Adobe Campaign.
* **Type / Size** - Defines the heading level of the title
* **Link** - Defines the content to which the title will link. This can be a path to a content page, an external URL, or a page anchor.
  * Click the Campaign icon to open the [Select Adobe Campaign Variable](/help/email/campaign-variables.md) dialog to insert dynamic content from Adobe Campaign.
* **ID** - This option allows controlling the unique identifier of the component in the HTML.
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS.

![Email Title Component's edit dialog](/help/email/assets/email-title-edit.png)

The in-place editor can also be used to edit the text of the title component.

![In-place editing of Email Title Component](/help/email/assets/email-title-edit-inline.png)

### Styles Tab {#styles-tab-edit}

The Email Title Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling)

Use the drop-down to select the styles that you want to apply to the component. Selections made in the edit dialog have the same effect as those chosen from the component toolbar.

Styles must be configured for this component in the [design dialog](#design-dialog) in order for the drop-down menu to be available.

![Styles tab of the edit dialog of Title Component](/help/email/assets/email-title-edit-styles.png)

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the default heading level that title components will have when created by the content authors.

### Sizes Tab {#sizes-tab}

![Title Component's design dialog](/help/email/assets/email-title-design.png)

* **Allowed Types / Sizes for Authors** - Enable or disable heading types that will be available for content authors when they use the Email Title Component.
* **Default Type / Size** - Define the heading type that will be automatically assigned when a content author adds the Email Title Component to a page.
* **Disable Link** - Disable support for links in the Email Title Component to disallow content authors from linking from titles.

### Styles Tab {#styles-tab}

The Email Title Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
