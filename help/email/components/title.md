---
title: Email Title Component
description: The Email Title Component is a section heading component for your emails that features in-place editing.
role: Developer, Admin, User
exl-id: f65b6973-bb36-406f-bbea-f85a23f5340b
index: false
TQID: https://experienceleague.adobe.com/wUhEpJH711SH3XHvCN31KaJnzBjwZKpxS85zqb5NGiU
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

|Component Version|AEM 6.5|AEM 6.5 LTS|AEM as a Cloud Service|
|---|---|---|---|
|v1|Compatible|-|-|

For more information about Core Component versions and releases, see the document [Core Email Components Versions](/help/versions.md).

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
