---
title: Adaptive Forms Core Component - Google reCAPTCHA
description: Enhance form security with Google reCAPTCHA service effortlessly with AEM Forms. Explain properties of Adaptive Form reCaptcha
role: Architect, Developer, Admin, User
---

# Adaptive Form reCAPTCHA {#google-recaptcha}

CAPTCHA (Completely Automated Public Turing Test to tell Computers and Humans Apart) is a program commonly used in online transactions to distinguish between humans and automated programs or bots. It poses a challenge and evaluates user response to determine if it's a human or a bot interacting with the site. It prevents the user to proceed if the test fails and helps make online transactions secure by keeping bots from posting spam or malicious purposes.

AEM Forms as a Cloud Service supports Google reCAPTCHA v2 in Adaptive Forms. You can use it to present a CAPTCHA challenge on form submission

## Usage {#reasons-to-use-google-recaptcha}


- **Spam and Bot Prevention**: One of the primary reasons to use reCAPTCHA is to prevent spam submissions and malicious bots from flooding your form. reCAPTCHA's advanced algorithms can detect automated attempts to submit the form, thus ensuring that only legitimate users can interact with it.

- **Enhanced Security**: By implementing reCAPTCHA, you add an extra layer of security to your adaptive form. This helps protect sensitive information and prevent malicious users from exploiting vulnerabilities.

- **User Experience**: While CAPTCHAs can sometimes be seen as an inconvenience, reCAPTCHA's adaptive approach means that most users are presented with a streamlined, user-friendly experience that requires minimal interaction. This can help maintain a positive user experience while still deterring bots.

- **Adaptability**: reCAPTCHA's adaptive mechanism analyzes user behavior and interactions to determine whether they are human or not. This means that the level of challenge presented to the user can vary based on the likelihood of them being a bot. This adaptability reduces friction for genuine users while maintaining strong security.

- **Reduced Manual Moderation**: By significantly reducing the number of spam submissions and bot-generated content, reCAPTCHA can save time and resources that would otherwise be spent on manual moderation and clean-up.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Google reCAPTCHA Core Component was released in Aug 2023 as part of the Core Components 'version'. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:


|Component Version|AEM as a Cloud Service|
|--- |--- |
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Google reCAPTCHA Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your Google reCAPTCHA experience for visitors with the Configure Dialog. You can also define Google reCAPTCHA options with ease for a seamless user experience.

### Basic Tab {#basic-tab} 

![Basic Tab](/help/adaptive-forms/assets/recaptcha-basictab.png)

- **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

- **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.

- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title, formatting options become visible to style the component's title. To access all available formatting options, you can click on the ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png)

- **Hide Title** - Select the option to hide the component's Title.
- **Mark as Unbound Form Element**: Select the option to configure a form field not linked to any schema. This option allows you to save data without updating the data source. It also enables you to handle data in a custom way, separate from standard database integration.
- **Configuration settings**: Select the configuration container that contains the cloud configuration connecting AEM Forms with the reCAPTCHA service by Google.
    
    >[!NOTE]
    >
    > Refer to the [Use Google reCAPTCHA in an AEM Adaptive Form based on Core Components](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components) article to learn how to create and configure Google reCAPTCHA for your environment.

- **Type**: Choose this option to select the size for reCAPTCHA.
    - **Normal**: Refers to the standard, larger version of the reCAPTCHA widget, which may be more visible and easier for users to interact with, especially on devices with larger screens.
    - **Compact**: Refers to a smaller version of the reCAPTCHA widget. This option is suitable for situations where space is limited, such as on mobile devices or in tight layouts on webpages.

- **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 

- **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The data of the disabled component is not submitted The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

- **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

### Validation Tab {#validation-tab}

![Validation Tab](/help/adaptive-forms/assets/recaptcha-validationtab.png)

-   **Error Message** - This option allows you to enter a message that is displayed if the **Required** checkbox is checked and the form field is left blank.

-   **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails.

## Design Dialog {#design-dialog}

Design Dialog is used to define and manage CSS styles for the reCAPTCHA component.

### Styles Tab {#styles-design-tab}

The Adaptive Forms reCAPTCHA Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

![Design Dialog](/help/adaptive-forms/assets/checkbox-style.png)

- **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms reCAPTCHA Core Component. 

- **Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.

### Custom Properties 

![Custom Properties Dialog](/help/adaptive-forms/assets/checkbox-customproperties.png)

Custom properties allow you to associate custom attributes (key-value pairs) to an Adaptive Form core component using the form template. The custom properties are reflected in the properties section of the headless rendition of the component. It allows creating dynamic form behavior that adapts based on the custom attributes values. For example, developers can design various renditions of a Headless Forms component for mobile, desktop, or web platforms, significantly enhancing the user experience across a wide array of devices.
- **Group Name**: You can provide a name to identify the custom property group. You can add, delete, or rearrange multiple custom property groups. After adding the custom property group, you can see the following options:

    - **Key-Value Pairs**: You can add multiple custom property names and custom property values by clicking the **Add** button for each custom property group.

    - **Delete**: Tap or click to delete the custom property name and custom property value.

    - **Rearrange**: Tap or click and drag to rearrange the custom property name and custom property value.


## Related Articles {#related-articles}

{{more-like-this}}

## See Also {#see-also}

{{see-also}}
