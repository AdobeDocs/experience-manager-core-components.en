---
title: Email Button Component
description: The Email Button component allows for the configuration and display of a button item in your content.
role: Developer, Admin, User
exl-id: b144e8d1-1097-475d-b2eb-3353c176afb9
index: false
TQID: https://experienceleague.adobe.com/-kCXMMJi8n6DSMh97cgqruQY8pI04AkhxO2GEvwaK6s
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
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
    internal-label: Accessibility
---
# Email Button Component {#email-button-component}

The Email Button component allows for the configuration and display of a button item in your content.

## Usage {#usage}

The Email Button component allows for the inclusion of a button in your content, clickable by the content reader, linking to additional resources.

* The button's properties can be selected in the [configure dialog.](#configure-dialog)
* Styles for the Email Button Component can be defined in the [design dialog.](#design-dialog)

## Version and Compatibility {#version-and-compatibility}

The current version of the Email Button Component is v1, which was introduced with release x of the Email Core Components in October 2022, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.5|AEM 6.5 LTS|AEM as a Cloud Service|
|---|---|---|---|
|v1|Compatible|-|-|

For more information about Core Component versions and releases, see the document [Email Core Components Versions.](/help/email/versions.md)

## Technical Details {#technical-details}

The latest technical documentation about the Email Button Component [can be found on GitHub.](https://adobe.com/go/aem_cmp_tech_email_button_v1)

Further details about developing Core Components can be found in the [Core Components developer documentation.](/help/developing/overview.md)

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the button and how it behaves and appears for a reader of your content.

### Properties Tab {#properties-tab}

![Properties tab of the edit dialog of Button Component](/help/email/assets/email-button-edit-properties.png)

* **Text** - The text to display on the button
  * Click the Campaign icon to open the [Select Adobe Campaign Variable](/help/email/campaign-variables.md) dialog to insert dynamic content from Adobe Campaign.
* **Link** - Link to a content page within AEM, an external resource, or an anchor
  * Use the **Selection Dialog** to choose a path within AEM.
  * Click the Campaign icon to open the [Select Adobe Campaign Variable](/help/email/campaign-variables.md) dialog to insert dynamic content from Adobe Campaign.
* **Icon** - Identifier for displaying an icon in the button
* **ID** - This option allows control of the unique identifier of the component in the HTML.
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting content.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS.
* **Open link in new tab** - If checked, the link will open in a new browser tab.

### Accessibility Tab {#accessibility-tab}

![Accessibility tab of the edit dialog of Button Component](/help/email/assets/email-button-edit-accessibility.png)

On the **Accessibility** tab, values can be set for [ARIA accessibility](https://www.w3.org/WAI/standards-guidelines/aria/) labels for the component.

* **Label** - Value of an ARIA label attribute for the component

### Styles Tab {#styles-tab-edit}

The Email Button Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling).

Use the drop-down to select the styles that you want to apply to the component. Selections made in the edit dialog have the same effect as those chosen from the component toolbar.

Styles must be configured for this component in the [design dialog](#design-dialog) in order for the tab to be available.

## Design Dialog {#design-dialog}

### Styles Tab {#styles-tab}

The Email Button Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
