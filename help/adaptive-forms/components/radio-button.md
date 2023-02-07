---
title: Adaptive Forms Core Component - Radio button
description: Using or customizing the Adaptive Forms Radio button Core Component.
role: Architect, Developer, Admin, User
---

# Radio button {#radio-button-adaptive-forms-core-component}

A radio button in an Adaptive Form is a type of input element that allows a user to select one option from a group of related options. It is represented by a small circular button that is either filled or empty to indicate whether the option is selected or not. When a user selects one radio button, the others in the group become deselected. Radio buttons are typically used when there are multiple mutually exclusive options and only one can be selected at a time.

**Example**

![](/help/adaptive-forms/assets/radio-button.png)

**Properties Dialog**

![](/help/adaptive-forms/assets/radio-button-properties.png)

In this example, Options element is used to group the radio buttons together. The **Display text** element is used to provide a label for an item and **Data Value** is used to specify the value that is sent to the server when the form is submitted. 

Each radio button option has a unique Data value and Display Text attribute. If a user selects the "1-10", the corresponding Data Value is sent to the server when the form is submitted. This data can then be processed by a server-side script to determine which options were selected by the user, and can be used to perform various actions, such as updating other fields in the form or submitting the form data to a server-side script for further processing.

Additionally, The each radio button can be configured to have different processing values for each option, and this can be set by using Adaptive Forms Rule Editor

## Usage {#reasons-to-use-radio-button}

There are several reasons to use radio buttons in a form, including:

*   **Limited choices**: Radio buttons are used to provide a list of predefined options for the user to choose from, and only one option can be selected at a time. This is useful when the number of options is limited and mutually exclusive.

*   **Clear representation**: Radio buttons are clear and easy to understand, making it simple for users to know what they are selecting.

*   **Consistency**: Using radio buttons ensures a consistent and standardized way of presenting options to users, making it easier for them to understand and interact with the form.

*   **Easier to use**: Radio buttons are easy to use, especially for users who are not familiar with technology, or who have limited mobility.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Radio Button Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Radio button Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/radiobutton/v1/radiobutton). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your Radio button experience for visitors with the Configure Dialog. You can also define Radio button options with ease for a seamless user experience.

## Design Dialog {#design-dialog}
