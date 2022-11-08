---
title: Using the Email Core Components
description: Learn about the basic installation, configuration, and usage of the Email Core Components.
role: Architect, Developer, Admin, User
hidefromtoc: yes
index: no
exl-id: 0e79ca8f-eb0a-4519-b1e8-a9d3b0b99987
---
# Using the Email Core Components {#using}

Learn about the basic installation, configuration, and usage of the Email Core Components.

## Installing the Email Core Components {#installation}

The Email Core Components can be used with AEM 6.5. See the [Requirements section of the Email Core Components Introduction document](introduction.md#requirements) for more information.

### Install Core Components {#core-components}

The Email Core Components are built on the AEM Core Components. Because the Core Components are not shipped with AEM, you must first install the AEM Core Components before installing the Email Core Components.

See the section [Download and Install](/help/get-started/using.md#download-and-install) section of the document Using Core Components for details on how to install the Core Components.

### Install Email Core Components {#email-core-components}

Once the Core Components are installed in your instance, you must likewise install the Email Core Components. The Email Core Components are not yet part of the AEM Project Archetype, so you will need to add them manually to your project. Follow the documentation in [the Email Core Components GitHub wiki to install.](https://github.com/adobe/aem-core-email-components/wiki/Adding-to-Existing-Project)

You can follow these same instructions if you wish to adapt an existing project to use the Email Core Components.

## Configuration {#configuration}

After installing the Core Components, you should complete two important configuration steps.

### Configure Campaign {#configure-campaign}

You must set up the AEM-Adobe Campaign integration in order for the two solutions to communicate.

* Configure your Adobe Campaign integration
  * Adobe Campaign Classic: [Integrating with Adobe Campaign Classic](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignonpremise.html)
  * Adobe Campaign Standard: [Integrating with Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html)
* [Link the Adobe Campaign integration configuration](/help/email/components/page.md#cloud-services-tab) to the content page where you will use the Email Core Components

### Add AEM Resource Type Filter for Email Components {#aem-resource-filter}

In order for Adobe Campaign to be able to render emails based on the Email Core Components, a filter must be adjusted in Campaign.

1. Log into Adobe Campaign as an administrator using the client console.

1. Select **Tools** -&gt; **Explorer** from the menu bar.

1. In the explorer, navigate to the **Administration** -&gt; **Platform** -&gt; **Options** node.

1. Select the `AEMResourceTypeFilter` option from the list.

1. In the **Value** field, append `core/email/components/page/<v1>/page` if it is not already present.

   * Replace `<v1>` with the current version of the Email Core Components [Page Component](/help/email/components/page.md) such as `v1`. 
   * Note that values in the **Values** field must be comma-delimited.

1. Click **Save**.

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
