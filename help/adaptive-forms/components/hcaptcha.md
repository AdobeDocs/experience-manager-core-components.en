---
title: hCaptcha in AEM Adaptive Forms
description: Enhance form security with hCaptcha&reg; service effortlessly. Step-by-step guide inside!
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
---
# hCaptcha Component{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> This feature is under the Early Adopter Program. You can write to aem-forms-ea@adobe.com from your official email id to join the early adopter program and request access to the capability. </span>

hCaptcha&reg; service protects your forms from bots, spam, and automated abuse. It poses a checkbox widget challenge and evaluates the user response to determine if it's a human or a bot interacting with the form. It prevents the user to proceed if the test fails and helps make online transactions secure by keeping bots from posting spam or malicious activities.

![hCaptcha&reg;](/help/adaptive-forms/assets/hCaptcha-challenge.png)

## Usage {#usage}

There are several reasons why it is beneficial to include a hCaptcha challenge in a form submission process, these are:

- **Bot Prevention**: It ensures that the form is being submitted by a human, reducing spam and automated submissions.

- **Security**: It adds an extra layer of security, verifying the legitimacy of each form submission and protecting against malicious attacks.

- **Data Integrity**: By preventing multiple or fraudulent submissions, It help to maintain the integrity and accuracy of the data collected through the form.

- **User Verification**: It verifies the identity of the user submitting the form, ensuring that only authenticated users can complete sensitive transactions.

- **Load Management**: It helps manage server load by controlling the rate of form submissions, preventing system overload during high-traffic periods.

## Technical Details {#technical-details}

Get the latest information about the hCaptcha Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

Specify the properties of hCaptcha Component by using the [configure dialog](#configure-dialog). The configure dialog is a part of the core components that are built to make the authoring of the forms easy and provide an efficient way to create complex forms.

## Version and Compatibility {#version-and-compatibility}


The Adaptive Forms hCaptcha Component is released in May 2024 as part of the [Core Components 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491). Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|||
|---|---|
|Component Version|AEM as a Cloud Service|
|--- |--- |
|v1|Compatible with<br>[release 2.0.4](/help/adaptive-forms/version.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.

## Configure Dialog {#configure-dialog}

You can easily customize properties of your hCaptcha Component with its Configure Dialog that has Basic Tab and Validation Tab for customizing various properties.

### Basic Tab {#basic-tab} 

- **[!UICONTROL Name]:** Specify the name for your hCaptcha component, you can identify a form component easily with its unique name both in the form and in the rule editor.
- **[!UICONTROL Title]:** Specify the title of your hCaptcha component.
- **[!UICONTROL Configuration Settings]:** Select a Cloud Configuration configured for hCaptcha&reg;.
- **Captcha Size:** You can select the display size of the hCaptcha&reg; challenge dialog box. Use the **[!UICONTROL Compact]** option to display a small sized and the **[!UICONTROL Normal]** option to display a relatively large-size hCaptcha&reg; challenge dialog.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

    ![hCaptcha Basic Tab](/help/adaptive-forms/assets/hcaptcha-basic.png)

### Validation Tab {#validation-tab}

- **[!UICONTROL Validation Message]:** Provide a validation message for your Captcha validation on the form submission.
- **[!UICONTROL Script Validation Message]** - Use this option to enter a prompt message, if the script validation fails.

    ![hCaptcha Validation Tab](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**hCaptcha&reg; is a registered trademark of Intuition Machines, Inc.**

**Know more** about other **Captcha Components** and their services, such as:

- [Use hCaptcha in an Adaptive Form for Core Components](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/integrate-adaptive-forms-hCaptcha-core-components/)

- [Use hCaptcha in an Adaptive Form for Foundation Components](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/integrate-adaptive-forms-hCaptcha/)

- [Use Turnstile CAPTCHA in an Adaptive Form for Foundation Components](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/integrate-adaptive-forms-turnstile/)

- [Use Google reCAPTCHA in an Adaptive Form for Foundation Component](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## Related Articles {#related-articles}

{{more-like-this}}

## See Also {#see-also}

{{see-also}}