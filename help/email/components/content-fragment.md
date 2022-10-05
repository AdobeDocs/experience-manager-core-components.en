---
title: Email Content Fragment Component
description: The Email Content Fragment component allows for the display of a content fragment in your content.
role: Architect, Developer, Admin, User
---

# Email Content Fragment Component {#email-content-fragment-component}

The Email Content Fragment component allows for the display of a [content fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) in your content.

## Usage {#usage}

The Email Content Fragment Component allows for the inclusion of a [content fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) in your email content. Content fragments are multichannel structured content that can be centrally authored and easily reused.

* The fragment and its properties can be selected in the [configure dialog.](#configure-dialog)
* Resource types to handle certain images and grids can be defined in the [design dialog.](#design-dialog)
* The edit option opens the selected fragment within the [content fragment editor,](#edit-dialog) customized for use with the Email Core Components.

## Version and Compatibility {#version-and-compatibility}

The current version of the Email Content Fragment Component is v1, which was introduced with release X of the Email Core Components in October 2022, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.5|AEM as a Cloud Service|
|---|---|---|
|v1|Compatible|Compatible|

For more information about Email Core Component versions and releases, see the document [Email Core Components Versions.](/help/email/versions.md)

## Sample Component Output {#sample-component-output}

To experience the Email Content Fragment Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library.](https://adobe.com/go/aem_cmp_library_email_cf)

## Technical Details {#technical-details}

The latest technical documentation about the Email Content Fragment Component [can be found on GitHub.](https://adobe.com/go/aem_cmp_tech_email_cf_v1)

Further details about developing Core Components can be found in the [Core Components developer documentation.](/help/developing/overview.md)

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define which content fragment and the elements of that fragment to be included.

### Properties Tab {#properties-tab}

![Email Content Fragment Component](/help/email/assets/email-content-fragment-edit-properties.png)

* **Content Fragment**

  * Path to the desired content fragment
  * The **Selection Dialog** can be used to locate the fragment

* **Display Mode**
  * **Single Text Element** - Enables selection of one multiline text element and enables paragraph control options
* **Variation** - Which variation of the content fragment to use (defaults to **Master**)

* **ID** - This option allows controlling the unique identifier of the component in the HTML.
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting content.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS.

### Paragraph Control Tab {#paragraph-control-tab}

![Email Content Fragment Component](/help/assets/content-fragment-edit-paragraph.png)

* **Paragraphs** - Allow selection of all paragraphs or a range
  * **All** - Display all paragraphs
  * **Range**
    * Specify ranges of paragraphs which should be displayed, separated by a semicolon
    * For instance `1;3-5;7;9-*` to include the first, the third to fifth, the seventh, and the ninth to the final paragraphs
* **Handle heading as their own paragraphs**

## Edit Dialog {#edit-dialog}

Once you have used the Email Content Fragment Component to configure a content fragment, when you select the component in the content editor, it shows an **Edit** option.

![Toolbar of Email Content Fragment Component](/help/email/assets/email-content-fragment-edit-toolbar.png)

Tapping or clicking the **Edit** button opens the content fragment editor. The content fragment editor has been extended to include buttons for the **Select Adobe Campaign Variable** to insert Adobe Campaign variables into your content fragments.

![Content fragment editor for email](/help/email/assets/email-content-fragment-editor.png)

For more information about editing and authoring content fragments, see the document [Authoring Fragment Content.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments-variations.html)

## Design Dialog {#design-dialog}

When an Email Content Fragment Component is configured with a content fragment, when you select it in the content editor, the toolbar reveals a button to open the content fragment editor.


### Main Tab {#main-tab}

![Design dialog of the Email Content Fragment Component](/help/email/assets/email-content-fragment-design.png)

* **Internal responsive grid**

  * The Sling resource type that is used for the internal responsive grid

### Styles Tab {#styles-tab}

The Email Experience Fragment Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling)
