---
title: How to get sample themes and templates for AEM Forms?
description: AEM Forms Core Components provides sample adaptive form themes, templates, and form data models
solution: Experience Manager Forms
topic: Administration
role: Admin, User
level: Intermediate
exl-id: aef6e88b-dcae-4777-9893-9257d7702f43
---
# Sample Themes, Templates, and Form Data models {#sample-themes-templates-and-data-models}

[!DNL AEM Forms] Core Components provide ready-to-use sample themes, templates, and form data models to create versatile adaptive forms quickly. These also help form authors to learn the extensibility, adaptability, and responsiveness of [Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html) to create simple forms in no time and complex forms easily while connecting with the database seamlessly.

The sample themes, templates, and form data models included in the reference content package are:

|Templates | Themes | Form Data Models |
---------|----------|---------
| [Basic](#Basic) |[Canvas](#Canvas) |Microsoft&reg; Dynamics 365  |
| [Blank](#Blank) |[WKND](#WKND) |Salesforce |
| [Contact Us](#Contact-Us) |[Easel](#Easel) |  |
| [Contact details update](#Contact-Details-Update) |[FSI](#FSI)   |   |
| [Consent form](#Consent-Form)   |[Healthcare](#Healthcare) |  |
| [Log service request](#Log-Service-Request) |  |  |
| [Give feedback](#Give-Feedback)  |  |  |
| [Benefits enrollment](#Benefits-Enrollment)|  |   |
| [Employee benefits summary](#Employee-Benefits-Summary)  |   |   |
| [Request for account statement](#Request-for-Account-Statement) |   |   |
| [Safety inspection form](#Safety-Inspection)|   |   |
| [Quality control inspection](#Quality-Control-Inspection)|   |   |
| [Purchase request](#Purchase-Request) |  |  |

## Sample themes {#Sample-Themes}

Reference sample themes help authors to use, define, and customize styling to forms, authors with even a basic knowledge of CSS can customize the theme as per requirement.

**How to get these themes?**
You get these themes by using any one of the methods given below: 

1. [Deploying an AEM Archetype 45 project to your environment](#using-archetype-to-deploy-themes)
1. [Enabling core components and using front-end pipeline to deploy themes](#use-front-end-pipeline-to-deploy-themes)

>[!NOTE]
> When you use the first method to deploy themes, you can use themes. In the second method you can use and customize themes.

### Deploying an AEM Archetype 45 project to your environment {#using-archetype-to-deploy-themes}

You can get these themes by deploying an [AEM Archetype 45](https://github.com/adobe/aem-project-archetype) to your **AEM Forms as a Cloud Service** or **AEM 6.5** Forms environment.

### Enable core components and use front-end pipeline to deploy themes {#use-front-end-pipeline-to-deploy-themes}

1. To get these themes on **Forms as a Cloud Service** environment, [enable Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html) and use the [front-end pipeline](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html) to deploy these themes.
    
1. To get these themes on **AEM 6.5 Forms** environment, [enable Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/enable-adaptive-forms-core-components.html) and use the [Package Manager](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.html) to deploy these themes.

<!--

[Learn to use and customize themes in AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html). 

[Learn to use and customize themes in AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.html).

-->

The **out of the box** [Adaptive Form Core Components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html) themes are:

![OOTB themes](/help/adaptive-forms/assets/archetype-45-themes.png)

### Canvas {#Canvas}

Canvas theme is the default theme for forms, and emphasizes the use of basic colors, transparency, and flat icons. In the screenshot below, you can see how the Canvas theme looks.

![Canvas theme](/help/adaptive-forms/assets/Safety-Inspection-Theme-Canvas.png)

### WKND {#WKND}

WKND theme embodies a lively, imaginative, and engaging design to showcase a stylish appearance to your forms. The theme is based on the appearance and styling of [WKND site](https://wknd.site/us/en.html) which is a travel and adventure website build on [Adobe Experience Manager Core Components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html).

![WKND theme](/help/adaptive-forms/assets/Safety-Inspection-Form-Theme.png)


### Easel {#Easel}

Easel theme helps to create a form appearance that is appealing and easy to set up, it is customized for simplicity and user-friendliness. The easel theme is based on the concept where a portable stand is used by artists to support a canvas while they work on their paintings.

![Easel theme](/help/adaptive-forms/assets/Safety-Inspection-Theme-Easel.png)

### FSI (Financial Services & Insurance) {#FSI}

The FSI theme places an emphasis on giving your form a clean, practical look. The mild hue of blue are applied to your form when you apply the FSI theme, as you can see in the image.

![FSI Theme](/help/adaptive-forms/assets/fsi-theme-new1.png)


### Healthcare {#Healthcare}

The Healthcare theme employs rich, verdant tones to accentuate elements like tabs, panels, text boxes, and buttons within your form.

![Healthcare Theme](/help/adaptive-forms/assets/healthcare-new-theme.png)


## Sample templates {#Sample-templates}

Templates define initial form structure, content, and actions to replicate in your form or use a similar template structure to your form, for example, Consent form, Benefits enrollment form and many more. 

**How to get these templates?**
You can get these templates by deploying an [AEM Archetype 45](https://github.com/adobe/aem-project-archetype) to your **AEM Forms as a Cloud Service** or **AEM 6.5** Forms environment.

>[!NOTE]
>
> * If you have [enabled core components and used front-end pipeline to deploy themes](#use-front-end-pipeline-to-deploy-themes), you need not to deploy an AEM Archetype.
> * You can find list of all OOTB templates when you create a form.

The **out of the box** [Adaptive Form Core Components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html) templates are:

![Reference Templates](/help/adaptive-forms/assets/reference-templates-core-components.png)

### Basic {#Basic}

A basic template helps you quickly create an enrollment experience form. You can also use it to preview the functionality of [Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html). It provides a wizard layout for section-by-section presentation of data.

![Basic Template](/help/adaptive-forms/assets/Basic-template-desktop-view.png)

### Blank {#Blank}

A blank canvas template is used to create an Adaptive form structure, content, and rules from scratch. No form components are pre-incorporated in the blank template.
    
![Blank Template](/help/adaptive-forms/assets/Blank-temp-desktop-view.png)

### Contact Us {#Contact-Us}

Contact us form template is used to create a form to facilitate communication between website visitors and form administrators. Users can submit queries, feedback, or support requests through the form.

![Contact Us Template](/help/adaptive-forms/assets/Contact-us-desktop-view.png)

### Contact Details Update {#Contact-Details-Update}

Contact details update template help authors to create a form for address and contact details update of customers. The form also assists customers in updating personal information related to subscription or benefits to ensure seamless communication and uninterrupted access to the services or benefits.

![Contact-details-update](/help/adaptive-forms/assets/Contact-details-update.png)

### Consent Form {#Consent-Form}

The consent form template is used to create a form for procuring a legal document from participants who participate in a specific activity, research study, medical procedure, or any situation where their personal information or rights may be involved. The form ensures transparency, protect the rights of the participant, and establish a clear understanding of what the individual is agreeing to.

![Consent Form](/help/adaptive-forms/assets/Consent-form-desktop-view.png)

### Log Service Request {#Log-Service-Request}

Log service request template helps create a form that requests log-specific logging services from a service provider. The form serves as a formal request to create a ticket for events, activities, or data logs for monitoring or tracking status.

![Log Service Request Template](/help/adaptive-forms/assets/Log-service-request-desktop-view.png)


### Give Feedback {#Give-Feedback}

Give feedback form template helps to build a form to provide constructive feedback to another person or team. The form helps to ensure that feedback is clear, specific, and actionable, promoting open communication and improvement.

![Give Feedback Template](/help/adaptive-forms/assets/Give-feedback-desktop-view.png)


### Benefits Enrollment {#Benefits-Enrollment}

Benefits enrollment form template is used to create a form to collect essential information from their employees regarding their preferred benefits and coverage options. It typically accompanies the annual benefits enrollment period.

![Benefits Enrollment Template](/help/adaptive-forms/assets/Benefits-enrollment-form-template.png)


### Employee Benefits Summary {#Employee-Benefits-Summary}

Employee benefits summary form template is used to create a form to gather essential details about an individual's benefits. It helps in evaluating coverage quickly and accurately, providing a comprehensive overview for efficient assistance and support.
![Employee Benefits Summary](/help/adaptive-forms/assets/Employee-benefits-summary.png)


### Request for Account Statement {#Request-for-Account-Statement}  

A request for account statement template helps to create a form that initiates the process of obtaining an accurate and up-to-date statement of customers. The statement provides a detailed record of financial transactions, activities, or other relevant information about customers who use this form.

![Request-for-account-statment](/help/adaptive-forms/assets/Request-for-account-statment.png)

### Safety Inspection {#Safety-Inspection}

Safety inspection form template helps to create a form to input details for a safe work environment. By conducting regular inspections using this form, potential hazards can be identified. The form covers various aspects such as emergency exits, fire safety, electrical safety, hazardous materials, personal protective equipment, workstation ergonomics for the safety and well-being of employees, visitors, and customers.

![Safety Inspection Form](/help/adaptive-forms/assets/Safety-inspection-form.png)

### Quality Control Inspection {#Quality-Control-Inspection}

Quality control inspection form template is used to create a form to assess and document the visual appearance, dimensions, functionality, documentation, testing results, and overall quality of a product or item. It helps identify defects, non-conformances, and corrective actions necessary to ensure adherence to quality standards.

![Quality Control Inspection](/help/adaptive-forms/assets/Quality-Control-Inspection.png)


### Purchase Request {#Purchase-Request}

Purchase request form template helps to build a form to initiate the procurement process and allow employees to formally request the purchase of goods or services necessary for their work. The form captures essential details such as item description, quantity, preferred supplier (if applicable), budget allocation, justification for purchase, delivery information, and required approvals.

![purchase-request-form](/help/adaptive-forms/assets/Purchase-request-form.png)

## Reference Form Data Models {#reference-models}

After you create an Adaptive Form based on [Core Component](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html), you can connect your form with database Microsoft® Dynamics 365 and Salesforce servers to enable business workflows. For example:

* Write data in Microsoft&reg; Dynamics 365 and Salesforce on Adaptive Form submission.
* Write data in Microsoft&reg; Dynamics 365 and Salesforce through custom entities defined in Form Data Model and vice versa.
* Query Microsoft&reg; Dynamics 365 and Salesforce server for data and prepopulate Adaptive Forms.
* Read data from Microsoft&reg; Dynamics 365 and Salesforce server.

You can get the following Form Data Models by installing the [Reference content package](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-forms-reference-content.ui.content-2.1.0.zip):

* Microsoft&reg; Dynamics 365
* Salesforce 

For information on using these models, see [Configure Microsoft&reg; Dynamics 365 and Salesforce cloud services](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/configure-msdynamics-salesforce.html#configure-dynamics-cloud-service)
