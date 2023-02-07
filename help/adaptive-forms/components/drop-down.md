---
title: Adaptive Forms Core Component - Drop-down list
description: Using or customizing the Adaptive Forms Drop-down Core Component.
role: Architect, Developer, Admin, User
---

# Drop-down list {#drop-down-list-adaptive-forms-core-component}

A drop-down list in an Adaptive form allows users to select one or more option from a list of predefined options. The options can be of type String, Number, or Boolean. Additionally, the drop-down list component can be configured to have different validation and default values.

**Example**
![](/help/adaptive-forms/assets/drop-down-list.png)

## Usage {#reasons-to-use-drop-down-list}

There are several reasons why it is beneficial to include a drop-down list in an Adaptive Form, including:

*   **Limited options**: Drop-down lists are useful for situations where there are a limited number of options for a given field. They take up less space on the form than a list of radio buttons or checkboxes, and can be less overwhelming for users.

*   **Consistency**: Drop-down lists provide consistency in the design and layout of the form, making it more intuitive and easy for users to navigate.

*   **Clarity**: Drop-down lists can make the form more clear and easy to understand by providing a clear and concise list of options.

*   **User experience**: Drop-down lists can be used to make the form more user-friendly by providing a clear and intuitive way for users to select options.

*   **Data analysis**: Drop-down lists can be used to collect data from various sources and analyze it, or use it as input for further processing.


**Properties Dialog**

![](/help/adaptive-forms/assets/drop-down-list-properties.png)

In this example, Options element is used to define the list items. The **Display text** element is used to provide a label for list items and **Data Value** is used to specify the value that is sent to the server when the form is submitted. 

Each drop-down list option has a unique Data value and Display Text attribute. If a user selects the "Red" option, the corresponding Data Value is sent to the server when the form is submitted. This data can then be processed by a server-side script to determine which options were selected by the user, and can be used to perform various actions, such as updating other fields in the form or submitting the form data to a server-side script for further processing.

Additionally, The drop-down list can be configured to have different processing values for each option, and this can be set by using Adaptive Forms Rule Editor.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Drop-down list Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Drop-down list Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/dropdown/v1/dropdown). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your drop-down list experience for visitors with the Configure Dialog. You can also define drop-down list options with ease for a seamless user experience.

## Design Dialog {#design-dialog}

