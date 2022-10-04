---
title: Using the Email Core Components
description: 
role: Architect, Developer, Admin, User
---

# Using the Email Core Components {#using}

## Installing the Email Core Components {#installation}

The Email Core Components can be used with AEM 6.5 and AEM as a Cloud Service. See the [Requirements section of the Email Core Components Introduction document](introduction.md#requirements) for more information. However the installation steps will differ depending on on which type of AEM installation you have.

### AEM as a Cloud Service {#aemaacs}

Simply create an AEM project using the AEM project archetype.

### AEM 6.5 {#aem-65}

The Email Core Components are built on the AEM Core Components. Because the Core Components are not shipped with AEM, you must first install the AEM Core Components before installing the Email Core Components.

See the section [Download and Install](/help/get-started/using.md#download-and-install) section of the document Using Core Components for details on how to install the Core Components.
## Prerequisites {#prerequisites}

After installing the Core Components you should complete two important configuration steps:

* Configure your Adobe Campaign integration
  * Adobe Campaign Classic
    * AEM as a Cloud Service: [Integrating with Adobe Campaign Classic](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/integrating-campaign-classic.html)
    * AEM 6.5: [Integrating with Adobe Campaign Classic](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/integrating-campaign-classic.html)
  * Adobe Campaign Standard
* [Link the Adobe Campaign integration configuration](/help/email/components/page.md#cloud-services-tab) to the content page where you will use the Email Core Components

## Using the Email Core Components {#using-components}

Once the Email Components are installed and the integration with Adobe Campaign is configured, you can use the Email Components to create email content in AEM and then send that content to recipients using Adobe Campaign. The following is an overview of the workflow.

|Step|Description|Solution|
|---|---|---|
|1|Authors create a free-formed hierarchic structure of folders and email content as pages.|AEM|
|2|Using the [template editor,](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) authors configure an email header and/or footer that would be shared among all email pages resulting from this page template.|AEM|
|3|Authors use the [page editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/editing-content.html) to create email content using the text editor where they can pick Adobe Campaign variables and use the Segmentation Component to conditional show information if the recipient meets certain criteria.|AEM|
|4|When the email content is complete, [a workflow is run](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/workflows/overview.html) to approve the content and send to Campaign.|AEM|
|5|A delivery is created, defining a list of recipients.|Campaign|
|6|The content created in AEM is selected as the content of the delivery.|Campaign|
|7|The content is sent to the recipients, replacing the Adobe Campaign variables with the personalized information of the recipients.|Campaign|

For an example of creating email content in AEM and delivering in Adobe Campaign, please see the following resources.

* AEM as a Cloud Service: [Creating Campaign Newsletters with AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/campaign/creating-newsletters.html)
* AEM 6.5: [Working with Adobe Campaign Classic and Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html)

