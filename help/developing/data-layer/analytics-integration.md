---
title: Using Adobe Data Layer to Integrate Core Components and Adobe Analytics
description: How to configure Adobe Analytics to register Core Component events
---

# Using Adobe Data Layer to Integrate Core Components and Adobe Analytics {#analytics-integration}

This document details how to set up an end-to-end configuration based on AEM, the Adobe Data Layer, Adobe Launch and Adobe Analytics to track:

* The page ID stored in the Adobe Data Layer when a page is loaded
* The image path stored in the Adobe Data Layer when an image is clicked

This uses the core components as an example but can be used for your own custom components.

## Step 1 - Create the Report Suite in Adobe Analytics {#create-report-suite}

To aggregate and analyze your data, a report suite first must be created.

1. Go to `https://analytics.adobe.com`.
1. Sign in using your Adobe ID.
1. Click the **Analytics** icon.
1. Go to **Admin -&gt; Report Suites**.
1. Click **Create New -&gt; Report Suite**.
1. Fill the form:
   1. **Report Suite ID**: `yourSuiteID`
   1. **Site Title**: `Your suite description`
   1. **Time Zone**: As appropriate
   1. **Go Live Date**: today's date or as appropriate
   1. **Estimated Page Views Per Day**: 100 or as appropriate
1. Click **Create Report Suite**.

If successful you will receive the following message in green: `Report Suite <yourReportSuite> has been successfully created.`

## Step 2 - Make the Report Suite Visible {#make-visible}

To use the new report suite, it has to be visible.

1. Go to `https://adminconsole.adobe.com`.
1. Sign in using your Adobe ID.
1. Click the **Adobe Analytics - &lt;yourSite&gt;** card
1. Click the **Adobe Analytics - &lt;yourSite&gt;** link
1. Select the **Permissions** tab
1. Click the **Edit** button of the **Report Suites** row
1. Click the **+** button of the report suite you created in [step 1](#create-report-suite) to add it to the **Included Permission Items** category.
1. Click **Save**.

## Step 3 - Integrate Your AEM Site with Adobe Launch {#integrate-launch}

Launch must be integrated with your AEM site to generate data.

Follow the steps in the [Using Adobe Data Layer to Integrate Core Components and Adobe Launch](launch-integration.md) document.

## Step 4 - Install and Configure the Adobe Analytics Extension in Adobe Launch {#install-extension}

The Adobe Analytics Extension enables the integration of Analytics with Launch.

1. In Adobe Launch select the newly property that you created in [step 3.](#integrate-launch)
1. Navigate to the **Extensions** tab and select **Catalog**.
1. Search for **Adobe Analytics**.
1. Click **Install**.
1. Configure the extension.
   1. Enter the **Analytics Report Suite ID** created in [step 1](#create-report-suite) for the appropriate environments
   1. Set **Character Set** to UTF-8
1. Click Save

## Step 5 - Create a Data Element in Adobe Launch for the Page ID {#create-data-element}

A data element is required in Launch to be able to track the page ID.

1. In Adobe Launch select the property created in [step 3.](#integrate-launch)
1. Select the **Data Elements** tab and click **Add Data Element**:
   1. **Name**: `dl-page-id`
   1. **Extension**: **Core**
   1. **Data Element Type**: **Custom Code**
1. Click **Open Editor**
1. In the editor, enter the code: `return dataLayer.getState().page.id;`
1. Click **Save**.
1. Click **Save** to create the data element.

## Step 6 - Create a Rule in Adobe Launch to Track the Page ID in Analytics {#track-page}

Rules allow tracking of browsing attributes like page ID in Analytics.

Repeat the steps in Part 5b of the [Using Adobe Data Layer to Integrate Core Components and Adobe Launch](launch-integration.md#launch-rule) document to add the following rule in Adobe Launch:

* **Name**: `track-dl-page-id`
* EVENTS:
  * **Extension**: **Core**
  * **Event Type**: **Page Bottom**
* ACTION 1:
  * **Extension**: **Adobe Analytics**
  * **Action Type**: **Set Variables**
  * **prop1**: `%dl-page-id%`
* ACTION 2:
  * **Extension**: **Adobe Analytics**
  * **Action Type**: **Send Beacon**
  * Check **s.t(): Send Data to Adobe Analytics and treat it as a page view**

## Step 7 - Create a Rule in Adobe Launch to Register the Image Click Event {#register-click}

Rules allow tracking of browsing attributes like click events in Analytics.

Repeat the steps in Part 5b of the [Using Adobe Data Layer to Integrate Core Components and Adobe Launch](launch-integration.md#launch-rule) document to add the following rule in Adobe Launch:

* **Name**: `register-dl-image-click`
* EVENTS:
  * **Extension**: **Core**
  * **Event Type**: **Page Bottom**
* ACTION 1:
  * **Extension**: **Core**
  * **Action Type**: **Custom Code**
  * Editor: Enter the following code

```
    dataLayer.push({
        on: 'image clicked',
        handler: function(event, oldState, newState) {
          _satellite.track('dlImageClicked', event.info.path);
        }
    });
```

## Step 8 - Create a Rule in Adobe Launch to Track the Image Click Event in Analytics {#track-click}

Rules allow tracking of browsing attributes like click events in Analytics.

Repeat the steps in Part 5b of the [Using Adobe Data Layer to Integrate Core Components and Adobe Launch](launch-integration.md#launch-rule) document to add the following rule in Adobe Launch:

* **Name**: `track-dl-image-click`
* EVENTS:
  * **Extension**: **Core**
  * **Event Type**: **Direct Call**
  * **Identifier**: `dlImageClicked`
* ACTION 1:
  * **Extension**: **Adobe Analytics**
  * **Action Type**: **Set Variables**
  * **prop2**: Set as `%event.detail%`
* ACTION 2:
  * **Extension**: **Adobe Analytics**
  * **Action Type**: **Send Beacon**
  * Check **s.t(): Send Data to Adobe Analytics and treat it as a page view**

## Step 9 - Publish the Launch Code to Your Website {#publish-launch}

To enable the tracking of these rules and properties in Launch, the code must be published.

1. In the **Adobe Launch** tab, select the **Publishing** tab.
1. Click **Add New Library**.
1. As **Name** enter: `data-layer-analytics-1`.
1. As **Environment** select **Development (development)**.
1. Click **Add All Changed Resources**.
1. For each of the three rules (`track-dl-page-id`, `register-dl-image-click` and `track-dl-image-click`):
1. Select **Rules -&gt; rule -&gt; Latest** and click **Select &amp; Create a New Revision**.
1. Click **Save &amp; Build for Development**.

## Step 10 - Trigger Your Page to Send Information to Adobe Analytics {#trigger-page}

In this step you will install the Chrome extension **Launch and DTM Switch**. With this extension you only need to build and deploy the Launch code to the Development environment. There is no need to deploy the the Staging and Production environments.

1. Install the Chrome extension **Launch and DTM Switch** from Discovery.
1. Click the **Launch Switch** icon and set the Debug to *ON*.
1. Reload the page `http://<host>:<port>/content/core-components-examples/library/image.html`.
1. Open the browser console and you should see something similar to the following.

![Analytics Console output](/help/assets/analytics-console-output.png)

>[!TIP]
>
>You can also install the **Experience Cloud Debugger** extension for Chrome to view Adobe Launch and Analytics specific information about the page.

## Step 11 - View the Tracked Information in Adobe Analytics {#view-info}

Now you can view the events you triggered in Adobe Analytics.

1. Go to `https://analytics.adobe.com`.
1. Sign in using your Adobe ID.
1. Click the **Analytics** icon.
1. Select the **Reports** tab.
1. In the dropdown on the top right, select the report suite you created in [step 1.](#create-report-suite)
1. In the first column select **Custom Traffic -&gt; Custom Traffic 1-10 -&gt; Custom Insight 1** to view the tracked page IDs (paths) stored in the Data Layer. It should appear similar to the following.
  
   ![Custom insight 1](/help/assets/custom-insight-1.png)

1. Access the **Custom Insight 2** to view the tracked image paths stored in the Data Layer. It should appear similar to the following.

   ![Custom insight 2](/help/assets/custom-insight-2.png)
