---
title: Extending the Adobe Client Data Layer
description: The Adobe Client Data Layer can be extended following some basic patterns
feature: Core Components, Adobe Client Data Layer
role: Developer, Admin
exl-id: f3d5555b-4f08-49de-ab0f-dc0fb04aadf8
TQID: 'https://experienceleague.adobe.com/67YSpRfwNRMDgcBARHKLz51-Er6xb4vp1rXX0r0sbfE'
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: d9d38edd-df1b-480c-8f5e-72b62576f390
    internal-label: Site and page features
  - id: d429a63e-ade4-4117-b04e-9b996d1c94ef
    internal-label: Integrations
subfeature_v2:
  - id: c43ff1f6-5a6d-4e8c-b3cc-6bdb3fa6e092
    internal-label: Core components
  - id: a94e5c13-4138-47ec-b9c8-e804e17aaca2
    internal-label: Adobe Client Data Layer
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Extending the Adobe Client Data Layer {#extending-acdl}

You can extend the Core Components with custom dialog options that allow content authors to enter additional information related to the Data Layer.

To include these fields in the Data Layer that is provided by the Core Components, you must extend the model of the component that implements its own specific data layer methods.

## Example: Title Component {#example}

A Core Component like the [Title component](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) extends [Component](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) which has a `getData` method that by default returns [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serializes pre-defined fields that your component may implement, like `getDataLayerLinkUrl` and `getDataLayerTitle` for the [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Therefore, your custom Sling model might have a `getData` method that returns an object that extends `ComponentData` to return more fields.

Doing this, will add a `data-cmp-data-layer` attribute to the HTML element of your component with the JSON of the data that will be populated to the data layer. At this point, you can implement scripts that listen to this data or to related events.

>[!TIP]
>
>To further explore the flexibility of the Data Layer, review about the integration options including how to enable the Data Layer for your custom components.
