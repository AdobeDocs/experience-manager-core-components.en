---
title: Adaptive Forms Core Component - Title 
description: Using or customizing the Adaptive Forms Title Core Component.
role: Architect, Developer, Admin, User
---

# Title {#title-input-adaptive-forms-core-component}

In an Adaptive Form, a "title" refers to the text that appears at the top of the form, typically below the header. The title is specified using the Title component. This component can be added to the form layout, and its text can be edited to match the purpose or topic of the form. The title serves as a label or brief description of the form to the user, and it helps to distinguish the form from others.

**Example**

![](/help/adaptive-forms/assets/title.png)

## Usage {#reasons-to-use-title-in-an-adaptive-form}

There are several reasons why it's a good practice to use a title in a form:

*   **Clarity**: A title clearly identifies the purpose of the form, which helps users understand what information they need to provide.

*   **Organization**: A title can help to organize forms by topic or purpose, which makes it easier for users to find the form they need.

*   **Accessibility**: A title is a key element for users with accessibility needs, as it is read out loud by screen readers, helping users understand the context of the form.

*   **Branding**: A title can also be used to display a company or organization's name, which helps to create a sense of trust and familiarity with the user.

*   **Navigation**: A title can also be useful to navigate through the form, especially if the form is long or complex.

*   **Search Engine Optimization (SEO)**: Having a title on the form also helps in SEO, as search engines use the title to determine the relevance of a web page to a search query.

Overall, the title of a form is an important aspect of the user experience and it should be used to provide a clear and concise label for the form that helps users understand the context and purpose of the form.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Title Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Title Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/title/v1/title). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your title experience for visitors with the Configure Dialog. You can also define title options with ease for a seamless user experience.

![Basic tab](/help/adaptive-forms/assets/title_properties.png)

The edit dialog allows the content author to define the title text as well as select the heading level.

* **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.
* **Type /Size** - Defines the heading level of the title.
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the Data Layer.
    * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
    * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
    * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Design Dialog {#design-dialog}

Design Dialog is used to define and manage CSS styles for the Date-Picker component.

### Title

The Title Tab allows template authors to set default and allowed HTML heading elements for form authors: 

![Design dialog title tab](/help/assets/accordion-design-properties.png)

*   **Allowed Heading Elements**: A list with multiple options that lets the template author choose which headings elements can form author can use for Title.

*   **Default Heading Element**: A drop-down list that sets the default Heading element for Title component.


### Styles Tab {#styles-tab}

The Design Dialog is used to define and manage CSS styles for a component. The Adaptive Forms Date-picker Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

**Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Date-picker Core Component. 

**Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.

### Formats Tab {#format-tab}

The formats tab allows you to specify default and custom date formats. 

