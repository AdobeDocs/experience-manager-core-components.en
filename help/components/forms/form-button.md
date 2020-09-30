---
title: Form Button Component
description: The Core Component Form Hidden component allows for the inclusion of a hidden field in a form.
---

# Form Button Component {#form-button-component}

The Core Component Form Button Component allows for the inclusion of a button to trigger an action on a page.

## Usage {#usage}

The Core Component Form Button component allows for the creation of button field, often to trigger the submission of the form and is intended to be used along with the [Form Container component](form-container.md).

The button properties can be defined by the content editor in the [configure dialog](#configure-dialog).

## Version and Compatibility {#version-and-compatibility}

The current version of the Form Button Component is v2, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM as a Cloud Service|
|--- |--- |--- |---|
|v2|Compatible|Compatible|Compatible|
|[v1](/help/components/v1/form-button-v1.md)|Compatible|Compatible|-|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Form Button Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_form_button).

### Technical Details {#technical-details}

The latest technical documentation about the Form Button Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the parameters of the button.

### Properties Tab {#properties-tab}

![Form Button Component's edit dialog](/help/assets/form-button-edit.png)

* **Type**

  * **Button**
  * **Submit**

* **Title** - The text displayed on the button

  * If none provided it defaults to the button type

* **Name** - The name of the button, which is submitted with the form data
* **Value** - The value of the button, which is submitted with the form data

* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Design Dialog {#design-dialog}

### Styles Tab {#styles-tab}

The Form Button Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
