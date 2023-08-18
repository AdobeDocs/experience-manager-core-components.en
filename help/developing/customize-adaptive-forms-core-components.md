---
title: Customize Adaptive Forms Core Components
description: Learn to extend or create an Adaptive Forms Core Component to implement functionality tailored for your organization.
role: Architect, Developer, Admin
---

# Customize Adaptive Forms Core Components

Customizing Adaptive Forms Core Components allows you to tailor the out-of-the-box functionalities to fit your specific needs. This guide walks you through the process of customizing these components to create a more personalized experience. 

## Pre-requisite

Before diving into customizing Adaptive Forms Core Components,

* Learn about the [architecture of a Core Components](customizing.md#customizing-the-markup-customizing-the-markup) and go though the [official Adobe Experience Manager Core Components documentation](customizing.md). These comprehensive resources serve as your guide throughout the customization process.
* Set up your development environment This ensures a smooth workflow for making changes to the core components. While setting up the development environment, use an AEM Archetype project based on the latest AEM Archetype project. Based on your environment, you can: 
    
    * [Set up a local development environment for Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/setup-local-development-environment.html).  
    * [Set up a local development environment for AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html) 

## Customize an Adaptive Forms Core Component

Follow the steps below to modify the appearance, behavior, and functionality of an Adaptive Forms Core Component.

1. **Identify and duplicate the Core Component** 

    While configuring the development environment, you have created an Archetype-based project. In the AEM Archetype Project, identify the specific Core Component you wish to customize. Once identified, create a duplicate of the component within your AEM Archetype based project. Keep it in parallel to other Adaptive Forms Core Components. This step ensures that your customization efforts won't affect the original component, allowing you to experiment freely.

1. **Customize the Copied Component**

    Open the duplicated component and start making the necessary modifications according to your requirements:

    * **Customize HTML Structure**: Tailor the HTML structure to suit your design needs while adhering to [BEM (Block Element Modifier)](https://github.com/adobe/aem-core-wcm-components/wiki/css-coding-conventions) styling practices for maintainable and scalable code.
    * **Update label**: Update the label of the component to provide a clear and descriptive name for the customized version. Refer to the provided [OOTB (Out of the Box) label template](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/label.html) for consistency.
    * **Customize Widget**: Adjust the widget used within the component (dropdowns, checkboxes) to align with your specific use case. See, the [sample widget implementation](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/textinput.html) for reference.
    * **Help Text and Tooltips**: Personalize the help text or tooltips associated with the component to offer context and guidance to users. Use the [OOTB help text template](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/questionMark.html) as a starting point.
    * **Data Attributes**: Incorporate all necessary data attributes within the component's HTML elements. These attributes are crucial for the proper functioning of the component at runtime. Consult the [documentation](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput) to understand the role of data attributes in Adaptive Forms Core Components.

1. **Implement Backend Logic**

    If your customization requires backend logic, you can extend existing sling models. Refer to the provided [example](https://github.com/adobe/aem-core-forms-components/blob/master/bundles/af-core/src/main/java/com/adobe/cq/forms/core/components/internal/models/v1/form/TextInputImpl.java) to seamlessly integrate the desired functionality into your customized component.

1. **Configure the Component's Dialog**

    Configure the dialog associated with your customized component. Use the example [component dialog](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/_cq_dialog/.content.xml) provided in the documentation to ensure that user interactions and settings are appropriately managed.

1. **Deploy and test the component on your local development environment**

    Use [maven to build and deploy the component](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html#building-and-installing) on your local development environment. After the component is deployed, create an Adaptive Form to test the custom component. 

1. **Deploy the custom component on your production environment**

    After testing the component on your local development environment, deploy the component on your production environments. 

