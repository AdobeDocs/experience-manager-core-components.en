---
title: Adaptive Forms Core Component - Email input
description: Using or customizing the Adaptive Forms Email input Core Component.
role: Architect, Developer, Admin, User
---

# Email input {#email-input-adaptive-forms-core-component}

The Adaptive Form Email input Core Component is used to collect email addresses from users. It is typically represented as a text box and has pattern validations to accept only valid email addresses. The email input field can be further customized with additional attributes such as "required", "placeholder", and "pattern" to set validations for the input data.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

There are several reasons why it is beneficial to include a an email input component in an Adaptive Form, including: 

*   **Validation**: The email input field allows the browser to validate that the entered data is a valid email address format.

*   **User Convenience**: An email input makes it easier for users to enter their email addresses as it provides a clear indication of the data expected in the field.

*   **Personalized Communication**: Collecting email addresses from users through a form allows for personalized communication, such as sending confirmation emails or newsletters.

*   **Lead Generation**: By collecting email addresses through a form, businesses can build their email list and use it for lead generation.

*   **User Authentication**: Email addresses can be used as a means of authentication for accessing restricted content or services.

*   **Feedback Collection**: An email input in a feedback form allows the business to communicate with the user for follow-up or clarification on their feedback.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Email input Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Email input Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/emailinput/v1/emailinput). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your Email input experience for visitors with the Configure Dialog. You can also define Email input options with ease for a seamless user experience.

### Basic Tab {#basic-tab} 

![Basic tab](/help/adaptive-forms/assets/email_basictab.png)

* **Name** - The name uniquely identifies the component in the rule editor.Special characters and spaces are not allowed in the name strings.

* **Title** - Title is a string that appears at the top of a component in an Adaptive Form. Title uniquely identifies the component in the tree structure of an Adaptive Form. If you do not add a title, the name of the component is displayed instead of the title text.

* **Hide Title** - Select this option to hide title of the component type in an Adaptive Form.

* **Placeholder text** - 

* **Bind Reference** - This option allows you to link an Adaptive Form field to the schema. When user enters any value in a linked field of an Adaptive Form that value also appears in the associated schema.
* **Hide Component** - Select this option if you do not want to make the component type visible in an Adaptive Form. The component remains active in edit mode. 
* **Disable Component** - Select this option if you want to disable the component in an Adaptive Form. The component remains active in edit mode. 
* **Read-only** - Select this option if you want to make the component type immutable in an Adaptive Form. The component remains active in edit mode.

* **Default Value** - This option allows you to add a default value to your component type. The entered value appears by default at the place of the component type. If **Disabled Component** or **Read-Only Component** is selected, the default value is displayed on the screen.

### Validation Tab {#validation-tab}

![Validation tab](/help/adaptive-forms/assets/email_validationtab.png)

* **Required** - When this option is selected, the component type is displayed in an Adaptive Form. In the **Basic** tab, the **Hide Component** and **Disable Component** become non-clickable when this option is selected.

* **Error Message** -The option allows you to enter a message to be displayed if the required fields are left blank.

* **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails on an Adaptive Form submission.

* **Maximum Number of characters** - This option allows you to specify the maximum number of characters allowed  in the component type. If you enter a number of characters that is greater than the value specified in **Maximum Number of characters**, an error message appears on the screen. The **Maximum characters error message** dialog box allows you to add a custom error message.
 
* **Maximum characters error message** - The **Maximum characters error message** dialog box allows you to add a custom error message if you enter characters greater than the value specified in the **Maximum Number of characters** option.

    The **Validation Pattern** option allows you to enter a pattern to validate the entered email ID. The email ID entered is validated against the value entered in the **Pattern** option. In case the email Id fails to validate with the value entered in **Pattern** option , the error message appears on screen.
    * **Pattern** - This option allows you to enter the allowed verification patterns for email. Regular expressions are also allowed.
    * **Error Message** - This option allows you to enter a message that is displayed on the screen if the email ID fails to validate with the value entered in the **Pattern** option

### Help Content Tab {#help-content-tab}

![Help Content tab](/help/adaptive-forms/assets/email_helptab.png)

* **Short Description** - A short description provides enough context for the user to understand what the checkbox options convey. The entered text appears as a tool tip when the user hovers the mouse pointer over the component type. You can also format the text that appears in the short description.

* **Always show short description** - Select this option to display a short description even if the user does not hover over a component type.

* **Help Text** - Help text consists of information or error messages about the component type. Help text is available by clicking the icon that appears above the component type. Click the icon to display help text above the component type.You can also format the text that appears in the help section.

### Accessibility Tab {#accessibility-tab}

![Accessibility tab](/help/adaptive-forms/assets/email_accessibilitytab.png)

On the **Accessibility** tab, values are set for [ARIA accessibility](https://www.w3.org/WAI/standards-guidelines/aria/) labels for the component. Various options are available for using the text for screen reader:
* **Custom text**: Select this option to use the custom text for ARIA accessibility labels. Selecting this option displays the Custom Text dialog box. You can add relevant information in the Custom Text dialog box.
* **Description**: Select this option to use the description for ARIA accessibility labels.
* **Title**: Select this option to use the title for ARIA accessibility labels.
* **Name**: Select this option to use the name for ARIA accessibility labels.
* **None**: Select this option if you do not want to add for ARIA accessibility labels.




## Design Dialog {#design-dialog}

