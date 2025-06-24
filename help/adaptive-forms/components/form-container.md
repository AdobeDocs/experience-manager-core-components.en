---
title: Adaptive Forms Core Component - Form Container
description: Add an Adaptive Form to a Webpage.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
---

# Form container {#form-container-adaptive-forms-core-component}

<span class="preview"> This article discusses the **Drafts** <!--and **Hamburger Menu Support** --> feature, which is a pre-release feature. The pre-release feature is accessible only through our [pre-release channel](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html#new-features).</span>

Forms allow website visitors to interact with the website by providing valuable information, which can increase engagement and user satisfaction. An Adaptive Form Container in Adobe Experience Manager (AEM) Sites enables website owners to easily add forms to their pages. This helps facilitate communication between website visitors and the website owner or organization by providing a streamlined way for visitors to provide feedback, make inquiries, and complete other action

{{traditional-aem}}

## Usage {#reasons-to-use-forms-container}

There are several reasons why a form may be added to a website:
-   **Data collection**: Forms can be used to collect data from website visitors for various purposes, such as market research, user behavior analysis and more.

-   **Lead generation**: A form can be used to gather information from potential customers, such as name and email address, to generate leads for sales and marketing efforts.

-   **E-commerce**: Forms can be used for online shopping, allowing customers to place orders and make payments through the website.

-   **Contact**: A contact form allows website visitors to easily reach out to the website owner or organization.

-   **Surveys and polls**: Forms can be used to gather feedback and opinions from website visitors through surveys and polls.

-   **Event registration**: Forms can be used for event registration, allowing website visitors to sign up for events or webinars.

-   **Subscriptions**: Forms can be used for website subscriptions, allowing visitors to sign up for a newsletter or other regular communications.

-   **User authentication**: Forms can be used for user authentication, allowing website visitors to create accounts and log in to access exclusive content or features.

-   **Increase conversion rate**: A well-designed form can increase the conversion rate by making it easy for users to complete a desired action, like purchasing a product or signing up for a service.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Accordion Core Component was released in Feb 2023 as part of the Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 for AEM 6.5.16.0 Forms or later. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|AEM 6.5.16.0 Forms or later|
|---|---|---|
|v1|Compatible with<br>[release 2.0.4](/help/adaptive-forms/version.md) and later| Compatible with<br>[release 1.1.12](/help/adaptive-forms/version.md) and later but less than 2.0.0.|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Container Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your form container experience for visitors with the Configure Dialog. You can also define form container options with ease for a seamless user experience.

### Basic Tab {#basic-tab}

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab1.png)

-   **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.

- **Prefill services** - This option allows the user to select a prefill service for retrieving data when the Adaptive Form is rendered. Learn more about [how to create and configure a prefill service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=en#aem-forms-custom-prefill-service).

- **Role**: The role is an HTML attribute used to specify the purpose of an HTML element to assistive technologies such as screen readers. The role attribute is used to provide additional context and semantic meaning to an element, making it easier for screen readers to interpret and announce the content to the user. For example, in AEM Forms, a form field's label might have the role of "label," and its input field might have the role of "textbox." This helps the screen reader understand the relationship between the label and input field, and correctly announce them to the user.

-   **Client Library category** - The user can configure custom JavaScript library per Adaptive Form. It is recommended to keep only the reusable functions in the library, which have dependency on jquery and underscore.js third-party libraries.
At times, if there are **complex validation rules**, the exact validation script reside in custom functions and users calls these custom functions from field validation expression. To make this custom function library known and available while performing server-side validations, the form user can configure the name of AEM client library under the **[!UICONTROL Basic]** tab of Adaptive Form Container properties. 
User can configure customJavaScript library per Adaptive Form. In the library, only keep the reusable functions, which have dependency on jquery and underscore.js third-party libraries.

<!--
- **Enable the hamburger menu for mobile view** - Select the checkbox to integrate a hamburger menu into your form for mobile view. Represented by three horizontal lines stacked vertically, this menu provides a clear and uncluttered display for panels on smaller devices, especially on mobile devices. For more information about the hamburger menu, refer to the [Learn more about the hamburger menu](#learn-more-about-the-hamburger-menu) section. -->


### Data Model Tab {#data-model-tab}

![Submission tab](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

You can use the Form Data Model to connect a form to a Data Source to send and receive data based on user actions. You can also connect a form to a JSON schema to receive the submitted data in a pre-defined format. Based on the requirement, connect your form to a JSON schema or Form data model:
- Create a JSON Schema and upload to your environment
- Create a Form Data Model

### Drafts

![Submission tab](/help/adaptive-forms/assets/formcontainer_autosavetab.png)

- **Automatically save drafts**: Select the **Automatically save drafts** check box to enable saving of forms as drafts.
- **Save Preference**: Configure **Save Preference** as **Save drafts at regular intervals**, to auto-save the form after a specific interval of time.
**Save interval frequency (Seconds)**: Specify the time interval (in seconds) to set the duration that triggers the automatic saving of the form at the defined interval.

### Submission Tab {#submission-tab}

Users can configure different actions for an Adaptive Form submissions. 

- **Redirect URL/Path** - This option allows user to configure a page for each form, to which the form users are redirected after submitting an Adaptive Form. Click here for more information on [how to configure redirect pages](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html).

![Submission tab](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

-   **Show Message** - This option allows users to add a message that is displayed when the Adaptive Form is successfully submitted. The predefined text is included in the dialog box and it can be modified by the user. The Show Message dialog supports rich text formatting tools that allow users to format the added text.

![Show Message tab](/help/adaptive-forms/assets/formconatiner_showmessage.png)   

-   **Submit Action** - A Submit Action is triggered when a user clicks the Submit button on an Adaptive Form. The users can select Submit Actions from the drop-down list that are supported out of the box. Learn how to [configure a Submit Action in the Submission tab](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#supporting-custom-functions-in-validation-expressions-br).

## Design Dialog {#design-dialog} 

Design Dialog is used to define and manage CSS styles for the Form Container component.

### Allowed Components Tab {#allowed-components-tab}

![Design dialog allowed component tab](/help/adaptive-forms/assets/formcontainer-allowedcomponents.png)

The **Allowed Components** tab allows template editor to set the components that can be added as items to the panels in the component in the Adaptive Forms editor.

### Default Components Tab {#default-components-tab}

![Design dialog default component tab](/help/adaptive-forms/assets/formcontainer-defaultcomponents.png)

The **Default Components** tab allows the template editor to specify the components that are visible by default as items in the form container component in the Adaptive Forms editor.

### Responsive Settings Tab {#responsive-tab}

![Design dialog responsive settings tab](/help/adaptive-forms/assets/formcontainer-responsivestyle.png)

The **Responsive Settings** tab allows the template editor to specify the number of columns in the grid within the form container component in the Adaptive Forms editor. 

### Styles Tab {#styles-tab}

The Adaptive Forms File Attachment Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

![Design Dialog](/help/adaptive-forms/assets/formcontainer-styletab.png)

- **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Form Container Core Component. 

- **Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.

### Custom Properties Tab

![Custom Properties Dialog](/help/adaptive-forms/assets/formcontainer-custompropertiestab.png)

Custom properties allows you to associate custom attributes (key-value pairs) to an Adaptive Form core component using the form template. The custom properties are reflected in the properties section of the headless rendition of the component. It allows creating dynamic form behavior that adapts based on the custom attributes values. For example, developers can design various renditions of a Headless Forms component for mobile, desktop, or web platforms, significantly enhancing the user experience across a wide array of devices.

- **Group Name**: You can provide a name to identify the custom property group. You can add, delete, or rearrange multiple custom property groups. After adding the custom property group, you can see the following options:

    - **Key-Value Pairs**: You can add multiple custom property names and custom property values by clicking the **Add** button for each custom property group.

    - **Delete**: Tap or click to delete the custom property name and custom property value.

    - **Rearrange**: Tap or click and drag to rearrange the order of the custom property name and custom property value.

<!--
## Learn more about the hamburger menu

A hamburger menu, often referred to as a mobile menu or navigation drawer, is a popular design element in mobile user interfaces. It features three horizontal lines stacked vertically, resembling a hamburger. The design efficiently conserves screen space by hiding secondary navigation options until they are needed, especially on smaller devices such as mobile. AEM forms can be efficiently organized within the hamburger menu, enabling users to access various panels within a form without overwhelming the main interface.

Consider a scenario, where a financial institution offers an online loan application form that requires users to provide detailed information across several panels, such as personal details, financial information, loan preferences, and supporting documents. The form includes multiple panels and options that can clutter the interface, especially on mobile devices. Users need an organized way to navigate through these panels without feeling overwhelmed. The hamburger menu is implemented to enhance the user experience on mobile devices.

### Components of hamburger menu

![Hamburger Menu](/help/adaptive-forms/assets/hamburger-menu.png){width=50%, align=center}

**A. Hamburger menu**: The hamburger menu features a navigation panel that slides out or drops down when the hamburger icon is clicked or tapped. The menu displays the panel headings, and selecting a panel shifts the focus to that panel. It allows users to easily navigate between different panels.

![Hamburger Menu](/help/adaptive-forms/assets/hamburger-menu-icon.png){width=50%}

**B. Breadcrumb**: Breadcrumbs indicate the user’s current location within the form. They offer a hierarchical trail that shows the user’s navigation path and helps them understand their position in the form.

**C. Active panel**: The active panel refers to the section or part of the form that is currently being displayed. When a user selects an option from the hamburger menu, the corresponding panel becomes the active panel, showing the relevant fields and information for that section.

### Points to consider while working with the hamburger menu

- The hamburger menu displays only the names of the panels. Here are different scenarios illustrating how the panel name appears in the navigation pane of the hamburger menu based on the configuration properties of the panel:  
  
  - If you set the properties of the panel to hidden, the panel's name does not appear in the navigation pane of the hamburger menu. For example, if you configure the properties of the `Financial Information` panel as `hidden`, the panel name does not appear in the navigation pane of the hamburger menu.
    
    ![Hidden panel](/help/adaptive-forms/assets/hidden-panel.png){width=50%}

  - If you set the properties of the panel to `disabled`, its name appears in the navigation pane of the hamburger menu, but you cannot select or edit it. For example, if you configure the properties of the `Financial Information` panel as `disabled`, the panel name appears in the navigation pane, but it cannot be selected or edited. 
     
    ![Disabled panel](/help/adaptive-forms/assets/disabled-panel.png){width=50%}

  - If you hide the  title of the panel, it does not appear in the navigation pane of the hamburger menu. A blank space shows up instead, but you can navigate to the fields of the panel by clicking on that space. For example, if you hide the title of the `Financial Information` panel, the blank space appears in its place in the navigation pane of the hamburger menu. You can navigate to the fields of the panel by clicking on the blank space.
    
    ![Hidden title panel](/help/adaptive-forms/assets/hidden-title-panel.png){width=50%}

- By default, the navigation pane in the breadcrumb component supports up to three levels of navigation. However, with the custom component, you can configure the navigation hierarchy to accommodate as many levels as needed.
- When using the hamburger menu, the user can navigate between panels using arrows. However, once a panel is selected, the menu automatically closes, and focus shifts to the fields within the chosen panel.

### Advantages to use hamburger menu

- **Space efficiency**: By hiding form navigation options until needed, the hamburger menu maximizes screen space, which is especially beneficial on smaller devices.

- **Clutter reduction**: It minimizes visual clutter by consolidating various form navigation links into a single, collapsible menu.

- **Improved focus**: With fewer visible navigation elements, users can concentrate on the main content of the form without being distracted by secondary options.

- **Simplified design**: It creates a more streamlined user interface, resulting in a cleaner and more organized form layout.

- **Enhanced mobile experience**: On mobile devices, where screen space is limited, the hamburger menu offers an efficient way to access all form navigation options without overwhelming the user.

### How to enable hamburger menu for your form?

To enable hamburger menu for form, perform the following steps:

1. Open form in an edit mode.
1. Open the Content browser, and select the **[!UICONTROL Guide Container]** component of your Adaptive Form. 
1. Click the Guide Container properties ![Guide properties](/help/adaptive-forms/assets/configure_icon.png) icon. The Adaptive Form Container dialog box opens. 
1. Click the  **[!UICONTROL Basic]** tab. 
1. Select the **[!UICONTROL Add hamburger menu support]** checkbox.
1. Click **[!UICONTROL Done]**.

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab.png)
-->

## Related Articles {#related-articles}

{{more-like-this}}

## See Also {#see-also}

{{see-also}}