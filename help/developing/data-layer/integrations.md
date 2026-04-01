---
title: Integrations and the Adobe Client Data Layer
description: Learn how the Adobe Client Data Layer can integrate with your custom components and how integrations with Adobe Analytics and Adobe Target can help you gain insights into your website
feature: Core Components, Adobe Client Data Layer
role: Developer, Admin
exl-id: 503dd3dc-fe95-4a17-83f5-1f0c1960993d
TQID: https://experienceleague.adobe.com/xncfOtz1FNyeH6CjQjg7cSeIonIg2mkBIPUgZvMI7Ww
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: ae478996-b206-4712-9b0c-dc78a2644453
    internal-label: Integrations
  - id: d429a63e-ade4-4117-b04e-9b996d1c94ef
    internal-label: Integrations
subfeature_v2:
  - id: a94e5c13-4138-47ec-b9c8-e804e17aaca2
    internal-label: Adobe Client Data Layer
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---
# Integrations with the Adobe Client Data Layer {#integrations}

The Adobe Client Data Layer reduces the effort to instrument websites by providing a standardized method to expose and access any kind of data for any script.

The Adobe Client Data Layer can integrate with your custom components and integrations with Adobe Analytics and Adobe Target can help you gain insights into your website.

## Enabling the Data Layer for Custom Components {#enabling-custom-components}

To automatically add a custom component to the Data Layer:

1. Define the properties of the custom component model that needs to be tracked.
1. Add the `data-cmp-data-layer` attribute to the custom component HTL. E.g. `data-cmp-data-layer="${mycomponent.data.json}"`.

To automatically make the Data Layer trigger a `cmp:click` event each time a specific element of the custom component is clicked, add the `data-cmp-clickable` attribute to the element to be tracked in the custom component HTL.

The `data-cmp-data-layer-enabled` attribute can be queried client-side to check if the data layer is enabled.

>[!TIP]
>
>For further technical details about the integration of the Adobe Client Data Layer with the Core Components and how to enable the Data Layer on your custom components, see the [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) file in the Core Components repository.

## Integrating with Adobe Analytics and Adobe Target {#analytics-target}

Paired with Adobe Analytics and Adobe Target, the Adobe Client Data Layer becomes the foundation of a very powerful and flexible tool set for gaining insights into your digital experiences. The following tutorials lead you through sample integrations.

### Collect Page Data with Adobe Analytics {#collect-page-data}

Learn to use the built-in features of the Adobe Client Data Layer with AEM Core Components to collect data about a page in Adobe Experience Manager Sites. Experience Platform Launch and the Adobe Analytics extension will be used to create rules to send page data to Adobe Analytics.

[View the tutorial here.](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html)

### Track Clicked Components with Adobe Analytics {#track-clicked-components}

Use the event-driven Adobe Client Data Layer with AEM Core Components to track clicks of specific components on an Adobe Experience Manager site. Learn how to use rules in Experience Platform Launch to listen for click events, filter by component and send the data to an Adobe Analytics with a track link beacon.

[View the tutorial here.](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html)
