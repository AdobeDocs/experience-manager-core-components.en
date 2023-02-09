---
title: Adaptive Forms Core Component - Tabs on top
description: Using or customizing the Adaptive Forms Tabs on top Core Component.
role: Architect, Developer, Admin, User
---

# Tabs on top {#tabs-on-top-adaptive-forms-core-component}

A tabs-on-top layout in an Adaptive Form is a way to organize and group related fields and sections of a form into separate tabs. Each tab is represented by a tab label, typically located at the top of the form, and contains a specific set of form fields and sections. This layout allows users to easily navigate and access different sections of the form, making it more user-friendly and less overwhelming. It is generally used when the form contains a lot of fields and sections, and it is necessary to divide them into smaller, manageable chunks. Tabs can also help to improve accessibility by allowing users to navigate the form using keyboard shortcuts, making it easier for users with disabilities to access the form.

**Example**

![](/help/adaptive-forms/assets/tabs.png)

## Usage {#reasons-to-use-tab-on-the-top-layout}

There are several reasons to use tabs on the top layout in an Adaptive Form:

*   **Organization**: Tabs can be used to organize different sections of a form into separate categories, making it easier for users to navigate and find the information they need.

*   **Space Conservation**: Tabs can help to conserve space on a page by allowing only one section of the form to be visible at a time.

*   **Improved User Experience**: Tabs can improve the user experience by making the form more visually appealing and easier to use.

*   **Mobile-friendly**: Tabs make forms more mobile-friendly by reducing scrolling and making it easy to switch between fields.

In short, Tabs can make forms more organized, space efficient, user-friendly and accessible.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Tabs on Top Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Tabs on Top Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/tabsontop/v1/tabsontop). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your tabs on top experience for visitors with the Configure Dialog. You can also define Tabs on top options with ease for a seamless user experience.

## Design Dialog {#design-dialog} 

The Design Dialog lets template creators control how things are displayed by default. For the Adaptive Forms Accordion component, you can set the following:

* The core components that a form creator can add to the accordion in the Adaptive Forms editor
* Simple names for styles (CSS classes) which can be applied in the properties dialog of Tabs on top component in the Adaptive Forms editor.

This helps make the process of creating and customizing forms more straightforward and efficient.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab allows template editor to set the components that can be added as items to the panels in the Tabs on top component in the Adaptive Forms editor.

### Styles Tab {#styles-tab}

The Design Dialog is used to define and manage CSS styles for a component. The Adaptive Forms Tabs on top Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

**Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Tabs on top Core Component. 

**Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.
