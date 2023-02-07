---
title: Adaptive Forms Core Component - Checkbox Group
description: Using or customizing the Adaptive Forms Checkbox Group Core Component.
role: Architect, Developer, Admin, User
---

# Checkbox Group {#button-component-adaptive-forms-core-component}

A checkbox group in an Adaptive Form is a set of related checkboxes that allow users to select one or more options from a list. Each checkbox is represented by a Data Value (value used to process items of a checkbox group) and Display value (label for each checkbox item that describes its purpose)

**Example**

![](/help/adaptive-forms/assets/checkbox-group.png)

**Properties Dialog**

![](/help/adaptive-forms/assets/checkbox-group-properties.png)

In this example, Options element is used to group the checkboxes together. The **Display text** element is used to provide a label for an item and **Data Value** is used to specify the value that is sent to the server when the form is submitted. 

Each checkbox option/item has a unique Data value and Display Text attribute. If a user selects the "Son" and "Daughter" checkboxes, the corresponding Data Value is sent to the server when the form is submitted. This data can then be processed by a server-side script to determine which options were selected by the user, and can be used to perform various actions, such as updating other fields in the form or submitting the form data to a server-side script for further processing.

Additionally, The checkbox group can be configured to have different processing values for each option, and this can be set by using Adaptive Forms Rule Editor.

## Usage {#reasons-to-use-check-box-group}

There are several reasons why it is beneficial to include a checkbox group in an Adaptive Form, including:

*   **Multiple selections**: A checkbox group allows users to select multiple options from a list, which can be useful in situations where multiple selections are allowed or required.

*   **User experience**: Checkbox group can be used to make the form more user-friendly by providing a clear and intuitive way for users to select multiple options.

*   **Data analysis**: Checkbox group can be used to collect data from various sources and analyze it, or use it as input for further processing.

*   **Surveys**: Checkbox group can be used in surveys to select multiple options for a question.

*   **User preferences**: Checkbox group can be used to collect user preferences for different options.

*   **Data Value**: Checkbox group can also be used to process items of a checkbox group.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Checkbox Group Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Checkbox Group Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your checkbox experience for visitors with the Configure Dialog. You can also define checkbox options with ease for a seamless user experience.

## Design Dialog {#design-dialog}

