---
title: Adaptive Forms Core Component - Form Container
description: Add an Adaptive Form to a Webpage.
role: Architect, Developer, Admin, User
hide: yes
hidefromtoc: yes
exl-id: 1e413ef3-7a6f-41fc-825d-dbe09ebaffe9
---
# Google reCPATCHA {#google-recaptcha}

CAPTCHA (Completely Automated Public Turing test to tell Computers and Humans Apart) is a program commonly used in online transactions to distinguish between humans and automated programs or bots. It poses a challenge and evaluates user response to determine if it's a human or a bot interacting with the site. It prevents the user to proceed if the test fails and helps make online transactions secure by keeping bots from posting spam or malicious purposes.

AEM Forms as a Cloud Service supports Google reCAPTCHA v2 in Adaptive Forms. You can use it to present a CAPTCHA challenge on form submission

## Usage {#reasons-to-use-google-recaptcha}


- **Spam and Bot Prevention**: One of the primary reasons to use reCAPTCHA is to prevent spam submissions and malicious bots from flooding your form. reCAPTCHA's advanced algorithms can detect automated attempts to submit the form, thus ensuring that only legitimate users can interact with it.

- **Enhanced Security**: By implementing reCAPTCHA, you add an extra layer of security to your adaptive form. This helps protect sensitive information and prevent malicious users from exploiting vulnerabilities.

- **User Experience**: While CAPTCHAs can sometimes be seen as an inconvenience, reCAPTCHA's adaptive approach means that most users are presented with a streamlined, user-friendly experience that requires minimal interaction. This can help maintain a positive user experience while still deterring bots.

- **Adaptability**: reCAPTCHA's adaptive mechanism analyzes user behavior and interactions to determine whether they are human or not. This means that the level of challenge presented to the user can vary based on the likelihood of them being a bot. This adaptability reduces friction for genuine users while maintaining strong security.

- **Reduced Manual Moderation**: By significantly reducing the number of spam submissions and bot-generated content, reCAPTCHA can save time and resources that would otherwise be spent on manual moderation and clean-up.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Google reCAPTCHA Core Component was released in Aug 2023 as part of the Core Components 'version'. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|||
|---|---|
|Component Version|AEM as a Cloud Service|
|--- |--- |
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Google reCAPTCHA Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your Google reCAPTCHA experience for visitors with the Configure Dialog. You can also define Google reCAPTCHA options with ease for a seamless user experience.

### Basic Tab {#basic-tab} 

- **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

- **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.

- **Hide Title** - Select the option to hide the component's Title.

- **Configuration** - 

- **Type** - 

- **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 

- **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The data of the disabled component is not submitted The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

- **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

### Validation Tab {#validation-tab}

- **Error Message** - This option allows you to enter a message that is displayed if the **Required** checkbox is checked and the form field is left blank.

## See Also {#see-also}

- [Create an AEM Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)
- [Add an AEM Adaptive Form to AEM Sites page](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)
- [Apply themes to an AEM Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html)
- [Add components to an AEM Adaptive Form](/help/adaptive-forms/introduction.md#adaptive-forms-core-components-components)
- [Use reCAPTCHA in an AEM Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms.html)
- [Generate PDF version (DoR) of an AEM Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components.html)
- [Translate an AEM Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-aem-translation-workflow-to-localize-adaptive-forms-core-components.html)
- [Enable Adobe Analytics for an Adaptive Form to track form usage](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/services/enable-adobe-analytics-adaptive-form-using-experience-cloud-setup-automation.html)
- [Connect Adaptive Form to Microsoft SharePoint](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#create-sharepoint-configuration)
- [Connect Adaptive Form to Microsoft Power Automate](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#microsoft-power-automate)
- [Connect Adaptive Form to Microsoft OneDrive](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#submit-to-onedrive)
- [Connect Adaptive Form to Microsoft Azure Blob Storage](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#submit-to-azure-blob-storage)
- [Connect Adaptive Form to Salesforce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/oauth2-client-credentials-flow-for-server-to-server-integration.html)
- [Use Adobe Sign in an AEM Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/use-adobe-sign/working-with-adobe-sign.html)
- [Add a new locale for an Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components.html)
- [Send Adaptive Form data to a database](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/data-integration.html)
- [Send Adaptive Form data to a REST endpoint](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#submit-to-rest-endpoint)
- [Send Adaptive Form data to AEM Workflow](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#invoke-an-aem-workflow)
- [Use Forms Portal to list AEM Adaptive Forms on an AEM website](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-forms-portal.html)

