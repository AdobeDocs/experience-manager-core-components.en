---
title: Using Adobe Data Layer to Integrate Core Components and Adobe Launch
description: How to configure Adobe Launch to register Core Component events using Adobe Launch
---

# Using Adobe Data Layer to Integrate Core Components and Adobe Launch {#launch-integration}

The Core Components can be integrated with Adobe Launch by using the Adobe Data Layer. This document describes how to configure Adobe Launch to track click events for image components as an example.

When configured, Launch will produce the following output in the browser console when a Core Image component is clicked.

![Console output example](/help/assets/launch-console-output.png)

## Launch Integration with AEM {#launch-aem}

First Adobe Launch must be integrated with your AEM site.

### Step 1 - Create an Integration in Adobe I/O {#create-io-integration}

First sign in to Adobe I/O to start configuring an integration.

1. Go to `https://console.adobe.io`.
1. Sign in using your Adobe ID.
1. In the Quick Start section click **Create integration**.
1. Select **Access an API** and click **Continue**.
1. Select **Experience Platform Launch API** below Adobe Experience Platform and click **Continue**.

### Step 2 - Create an IMS Configuration in AEM {#ims-configuration}

In AEM you need to define the integration that you began configuring in Adobe I/O.

1. Go to the AEM home page, click **Tools -&gt; Security -&gt; Adobe IMS Configurations**.
1. Click **Create**.
1. As **Cloud Solution**, select **Adobe Launch**.
1. Check **Create new certificate**.
1. Enter an alias for the certificate such as **aem-launch-certificate**.
1. Click **Create certificate** and in the pop-up click **OK** to create the certificate.
1. Click **Download Public Key** and in the pop-up click **Download**.

### Step 3 - Finish Adobe I/O Configuration {#finish-io}

With the certificate and key created in AEM IMS configuration, you can finish your Adobe I/O configuration.

1. Go back to the Adobe I/O console as in [step 1.](##create-io-integration)
1. In the **Create a new integration** window, enter a name and a description such as **AEM Launch data layer**.
1. Under **Public keys certificates**, upload the certificate that you created in [step 2.](#ims-configuration)
1. Select the **Launch - Prod profile**.
1. Click **Create integration**.
1. Click **Continue to integration details**. You will need these details later to finish the IMS configuration in your AEM instance.

### Step 4 - Finish IMS Configuration {#finish-ims}

With the Adobe I/O integration details, you can finish the AEM IMS configuration.

1. In the AEM tab, in the **Adobe IMS Technical Account Configuration** tab from [step 2,](#ims-configuration) click **Next**.
1. Enter a title such as **IMS configuration for Adobe Launch**.
1. In the Adobe I/O tab, copy the **API Key (Client ID)**.
1. In the AEM tab, paste the former copied key in the **API Key field**.
1. In Adobe I/O, click **Retrieve Client Secret** and copy it.
1. In the AEM tab paste it into the **Client Secret** field.
1. In the Adobe I/O tab, select the **JWT** tab and copy the URL such as `https://ims-na1.adobelogin.com`.
1. In the AEM tab, paste the URL into the **Authorization Server** field.
1. In the Adobe I/O tab, copy the JWT payload (the code between the braces).
1. In the AEM tab, paste it into the **Payload** field.
1. Click **Create** to create the IMS configuration in AEM.

### Step 5a - Create a Property in Adobe Launch {#create-property}

A property defines features that Launch can inject to your site.

1. Go to Adobe Launch at `https://launch.adobe.com`.
1. Sign in using your Adobe ID.
1. Click **New Property**.
1. Enter a name such as **Launch AEM Data Layer**.
1. Enter your domain.
1. Click **Save**.

### Step 5b - Create a Rule in Launch {#launch-rule}

Using the property you created, you can define a rule, which specifies what should happen when an action occurs.

1. Click the newly added property from [step 5](#create-property) **Launch AEM Data Layer**.
1. Select the **Rules** tab and click **Create New Rule**.
1. Enter a name such as **image-click**.
1. Click the **+** button below **Events**.
1. Select **Core** as **Extension**, **Click** as **Event Type** and enter **.cmp-image** as **CSS selector**.
1. Click **Keep Changes**.
1. Click the **+** button below **Actions**.
1. Select **Core** as **Extension**, **Custom Code** as **Action Type** and click **Open Editor**.
1. In the editor, enter the following code: `console.log("DOM click event tracked by Launch for image: ", event.target.src);`
1. Click **Save**.
1. Click **Keep Changes**.
1. Click **Save** to create the new rule.

### Step 6 - Publish the Launch Rule {#publish-rule}

To make the new rule available for your AEM site, you need to publish it.

1. In the **Adobe Launch** tab, select the **Publishing** tab.
1. Click **Add New Library**.
1. Enter a **Name** as appropriate such as **demo-1**.
1. For **Environment** select as appropriate, such as **Development (development)**.
1. Click **Add a Resource**.
1. Select **Rules -&gt; image-click -&gt; Latest** and click **Select &amp; Create a New Revision**.
1. Click **Save &amp; Build for Development**.
1. In the popup, click **Apply Updates and Continue**.
1. When the library is built, click the ellipsis icon and select **Submit for Approval**.
1. In the popup click **Submit**.
1. Click the ellipsis icon and select **Build for Staging**.
1. When the build is finished, click the ellipsis icon and select **Approve for Publishing**.
1. In the popup click **Approve**.
1. Click the ellipsis icon and select **Build &amp; Publish to Production**.
1. In the popup click **Publish**.

### Step 7 - Enable Cloud Configurations for Your Site {#enable-configurations}

To use the integration, it needs to be assigned in AEM as a cloud configuration.

1. In the AEM console, click **Tools -&gt; General -&gt; Configuration Browser**.
1. Check the **Core Components Examples** and click **Properties**.
1. Check the **Cloud Configurations** and click **Save &amp; Close**.

### Step 8 - Create a Launch Integration with Your Site in AEM {#launch-integration}

A Launch integration is necessary for AEM to work with Launch

1. In the AEM console, click **Tools -&gt; Cloud Services -&gt; Adobe Launch Configurations**.
1. Select **Core Component Examples** and click **Create**.
1. Enter a **Title** such as **Launch configuration**.
1. Select the IMS configuration that you created in [step 4.](#finish-ims)
1. As **Company** select as appropriate.
1. As **Property** select the newly added Launch property created in [step 5.](#create-property)
1. Move the **Include Production Code on Author** slider to the right and click **Next**.
1. Click **Next**.
1. Click **Next**.
1. Click **Create**.

### Step 9 - Connect Your AEM Site to the Launch Integration {#connect-aem}

For AEM to use the Launch integration it needs to be assigned as a cloud configuration.

1. In the AEM console, click **Sites** and check the **Core Component**s site.
1. Click **Properties**.
1. Select the **Advanced** tab.
1. As **Cloud Configuration**, select the **Core Components Examples** and click **Select**.
1. Click **Save &amp; Close**.

### Step 10 - Verify That the Launch Logic is Applied to the Page {#verify-launch}

Test that the steps so far have been successful.

1. Open the Image page of the Core Components Library in preview mode: `http://<lhost&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Click an image and verify that the message `A Core Image was clicked` is displayed in the browser console.

## Launch Integration with AEM and the Data Layer {#data-layer-launch}

Now that the Integration between AEM and Launch is set up, we can integrate with the Data Layer.

### Step 1 - Create a rule in Adobe Launch {#create-rule}

Repeat the steps in [step 5](#launch-rul) to add a new rule in Adobe Launch using the following values.

* Name: `image-click-data-layer`
* EVENTS: 
  * Extension: Core
  * Event Type: DOM Ready
* ACTIONS:
  * Extension: Core
  * Action Type: Custom Code
  * Code:
  
    ```
    function onImageClick(event, oldState, newState) {
        console.log("Data layer click event tracked by Launch for image: " + event.info.path);
        console.log("dataLayer.getState(): ", dataLayer.getState());
    }
    dataLayer.push({
        on: 'image clicked',
        handler: onImageClick
    });
      ```

### Step 2 - Publish the Launch Rule to Make It Available to Your AEM Site {#publish-rule-2}

Repeat the steps in [step 6](#publish-rule) to publish the new rule.

### Step 3 - Verify That the Launch Logic is Applied to the Page {#verify}

1. Open the Image page of the Core Components Library in preview mode: `http://<host&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Click an image and verify that the following message is displayed in the browser console:

   ![Data layer console output](/help/assets/data-layer-console-output.png)
