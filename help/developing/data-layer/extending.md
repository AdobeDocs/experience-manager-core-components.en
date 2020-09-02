---
title: Extending the Adobe Client Data Layer
description: The Adobe Client Data Layer can be extended following some basic patterns
---

# Extending the Adobe Client Data Layer {#extending-acdl}

You can extend the Core Components with custom dialog options that allow content authors to enter additional information related to the Data Layer.

To include these fields in the Data Layer that is provided by the Core Components, you must extend the model of the component that implements its own specific data layer methods.

## Example: Title Component {#example}

A Core Component like the [Title component](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) extends [Component](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) which has a `getData` method that by default returns [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serializes pre-defined fields that your component may implement, like `getDataLayerLinkUrl` and `getDataLayerTitle` for the [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Therefore, your custom Sling model might have a `getData` method that returns an object that extends `ComponentData` to return more fields.

Doing this, will add a `data-cmp-data-layer` attribute to the HTML element of your component with the JSON of the data that will be populated to the data layer. At this point, you can implement scripts that listen to this data or to related events.
