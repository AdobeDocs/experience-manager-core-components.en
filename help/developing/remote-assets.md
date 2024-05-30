---
title: Support for Remote Assets
description: Learn how to configure the Core Component Image and Teaser Components to support remote assets using Dynamic Media with OpenAPI.
role: Architect, Developer, Admin, User
exl-id: b462c1f3-a6c8-4a2a-abf4-d08ec82d4371
---

# Support for Remote Assets {#remote-assets-support}

Learn how to configure the Core Component Image and Teaser Components to support remote assets using Dynamic Media with OpenAPI.

>[!NOTE]
>
>Dynamic Media with OpenAPI was formerly known as Next Generation Dynamic Media. The functionality and usage is identical.

## Get the Latest AEM Version {#latest}

Support for remote assets using Dynamic Media with OpenAPI requires:

* AEM 6.5 SP 18+ or AEM as a Cloud Service
* Core Components release 2.23.2 or later

## Configure HTTPS {#https}

It is generally recommended to run all of your production AEM instances using HTTPs. However your local development environments may not be set up as such. However, remote assets using Dynamic Media with OpenAPI requires HTTPS in order to function.

[Use this guide](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/security/use-the-ssl-wizard.html) to configure HTTPS wherever you wish to use remote assets, including development environments.

## Configure OSGi {#osgi}

The location of the remote assets must be defined in an OSGi configuration. Configure the **Next Generation Dynamic Media Config** OSGi configuration as follows, replacing the values with those of your remote asset environment.

```text
imsClient="<ims-client-name>"
enabled=B"true"
imsOrg="<ims-org>@AdobeOrg"
repositoryId="<repo-id>.adobeaemcloud.com"
```

![The Next Generation Dynamic Media Config OSGi configuration window](/help/assets/remote-assets-osgi.png)

For details on how to configure OSGi, please see the following documents:

* [Configuring OSGi for Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi.html) for AEM as a Cloud Service
* [Configuring OSGi](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/configuring/configuring-osgi.html) for AEM 6.5

## Verify Configuration {#verify}

Now you can verify that the remote assets feature using Dynamic Media with OpenAPI is working. To do this, you can install the WKND sample site and Core Components.

* [Core Components](https://github.com/adobe/aem-core-wcm-components/releases/download/core.wcm.components.reactor-2.23.2/core.wcm.components.all-2.23.2.zip) release 2.23.2 or later is required.
* [WKND Sample site](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-3.2.0/aem-guides-wknd.all-3.2.0-classic.zip) release 3.2.0 or later is required.

Once the Core Components and WKND site are installed, you can test the feature on any WKND page.

1. Access the AEM instance using HTTPS.

1. Open a WKND demo page in the page editor such as `https://<host>:<httpsPort>/editor.html/content/wknd/language-masters/en/magazine/arctic-surfing.html`

1. Add an image component to the page.

1. In the Configure dialog of the component, uncheck the option **Inherit featured image from page** on the **Asset** tab and click **Pick**.

1. If the configuration is correct, a drop-down will appear with the options **Local** and **Remote**. Select **Remote**.

   ![Remote and local pick options for image selection](/help/assets/remote-asset-selection.png)

1. A dialog will open and you will need to authenticate to the remote service.

1. Once authenticated, an asset browser of the remote service will open. Select the desired asset and tap or click **Select**.

   ![Selecting a remote asset](/help/assets/remote-asset-picker.png)

The remote asset is added to your local AEM page and you have verified that the feature is correctly configured.

## Using Remote Assets {#using}

Once configured, remote assets can be selected where you would select assets using the Core Components such as in the [Image Component](/help/components/image.md) and the [Teaser Component.](/help/components/teaser.md)
