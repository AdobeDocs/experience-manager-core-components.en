---
title: Form Options Component
description: The Core Component Form options component allows for the selection from pre-defined options in various formats.
---

# Form Options Component {#form-options-component}

The Core Component Form Options component allows for the selection from pre-defined options in various formats.

## Usage {#usage}

The Core Component Form Options component allows for the submission of different types of options presented in many different ways and is intended to be used along with the [Form Container component](form-container.md).

The presentation of the options, labels, and individual options can be defined by the content editor in the [configure dialog](#configure-dialog).

## Version and Compatibility {#version-and-compatibility}

The current version of the Form Options Component is v2, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM as a Cloud Service|
|--- |--- |--- |---|
|v2|Compatible|Compatible|Compatible|
|[v1](/help/components/v1/form-options-v1.md)|Compatible|Compatible|-|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Form Options Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_form_options).

### Technical Details {#technical-details}

The latest technical documentation about the Form Options Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_form_options_v2).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the type of options that should be presented, labels, and which options are available.

![Form Options Component's edit dialog](/help/assets/form-options-edit.png)

* **Types** - How the options will be presented
  * **Checkboxes**
  * **Radio buttons**
  * **Drop-down**
  * **Multi-select drop-down**
* **Title** - The title that will be displayed as the label for the options
* **Name** - The name of the field submitted with the form data
* **Source** - Where the options are defined
  * **Local** - Defined within the component
    * Tap or click the **Add** button to add a value, **Delete** to remove a value
      * **Value** - The value saved when that option is selected when the form is submitted
      * **Text** - The label for the option displayed on the form
      * **Active** - The option is marked as selected when the form loads
      * **Disabled** - The option is not selectable but still displayed
  * **List** - A static list defined elsewhere in AEM is used for the options
    * **List** - The path of the static list in AEM
      * Use the Browse button to locate the list resource
  * **Data source** - A data source is used for the options
    * **Data source** - Resource type of the data source
* **Help message** - A hint for the user of what can be entered in the field
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Design Dialog {#design-dialog}

### Styles Tab {#styles-tab}

The Form Options Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
