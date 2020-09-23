---
title: Using the Adobe Client Data Layer with the Core Components
description: Using the Adobe Client Data Layer with the Core Components
---

# Using the Adobe Client Data Layer with the Core Components {#data-layer-core-components}

The goal of the Adobe Client Data Layer is to reduce the effort to instrument websites by providing a standardized method to expose and access any kind of data for any script.

The Adobe Client Data Layer is platform agnostic, but is fully integrated into the Core Components for use with AEM.

Like the Core Components, the code for the Adobe Client Data Layer is available on GitHub along with its developer documentation. This document gives an overview of how the Core Components interact with the Data Layer, but full technical details are deferred to the GitHub documentation.

>[!TIP]
>
>For further information about the Adobe Client Data Layer, [refer to the resources in its GitHub repository.](https://github.com/adobe/adobe-client-data-layer)
>
>For further technical details about the integration of the Adobe Client Data Layer with the Core Components, see the [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) file in the Core Components repository.

## Installation and Activation {#installation-activation}

As of Core Components release 2.9.0, the Data Layer is distributed with the Core Components as a clientlib. No installation is necessary.

However the Data Layer is not activated by default. To activate the Data Layer you must create a [context-aware configuration](/help/developing/context-aware-configs.md) for it:

1. Create the following structure below the `/conf` node:
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * Node type: `nt:unstructured`
1. Add a boolean property called `enabled` and set it to `true`.
1. Add a `sling:configRef` property to the `jcr:content` node of your site below `/content` (e.g. `/content/<mySite>/jcr:content`) and set it to `/conf/<mySite>`.

Once enabled, you can verify the activation by loading a page of the site outside of the editor. When you inspect the page you will see that the Adobe Client Data Layer is loaded.

## Core Components Data Schemas {#data-schemas}

The following is a list of schemas that the Core Components use with the Data Layer.

### Component/Container Item Schema {#item}

The Component/Container Item schema is used in the following components:

* [Breadcrumb](/help/components/breadcrumb.md)
* [Button](/help/components/button.md)
* [Language Navigation](/help/components/language-navigation.md)
* [List](/help/components/list.md)
* [Navigation](/help/components/navigation.md)
* [Teaser](/help/components/teaser.md)
* [Text](/help/components/text.md)
* [Title](/help/components/title.md)

The Component/Container Item schema is defined as follows.

```javascript
id: {                   // component ID
    @type               // resource type
    repo:modifyDate     // last modified date
    dc:title            // title
    dc:description      // description
    xdm:text            // text
    xdm:linkURL         // link URL
    parentId            // parent component ID
}
```

The following [event](#events) is relevant to the Component/Container Item schema:

* `cmp:click`

### Page Schema {#page}

The Page schema is used by the following component:

* [Page](/help/components/page.md)

The Page schema is defined as follows.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    xdm:tags            // page tags
    repo:path           // page path
    xdm:template        // page template
    xdm:language        // page language
}
```

### Container Schema {#container}

The Container schema is used by the following components:

* [Accordion](/help/components/accordion.md)
* [Tabs](/help/components/tabs.md)
* [Carousel](/help/components/carousel.md)

The Container schema is defined as follows.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    shownItems          // array of the displayed item IDs
}
```

The following [events](#events) are relevant to the Container schema:

* `cmp:click`
* `cmp:show`
* `cmp:hide`

### Image Schema {#image}

The Image schema is used by the following component:

* [Image](/help/components/image.md)

The Image schema is defined as follows.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    image               // asset detail (see below section)
}
```

The following [event](#events) is relevant to the Image schema:

* `cmp:click`

### Asset Schema {#asset}

The Asset schema is used inside the [Image component.](/help/components/image.md)

The Asset schema is defined as follows.

```javascript
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```

The following [event](#events) is relevant to the Asset schema:

* `cmp:click`

## Events {#events}

There are a number of events that the data layer triggers.

* **`cmp:click`** - Clicking a clickable element (an element that has a `data-cmp-clickable` attribute) causes the data layer to trigger a `cmp:click` event.
* **`cmp:show`** and **`cmp:hide`** - Manipulating the accordion (expand/collapse), the carousel (next/previous buttons), and the tabs (tab select) components causes the data layer to trigger `cmp:show` and a `cmp:hide` events respectively.
* **`cmp:loaded`** - As soon as the data layer is populated with the core components on the page, the data layer triggers a `cmp:loaded` event.

### Events Triggered by Component {#events-components}

The following tables list the standard Core Components that trigger events along with those events.

|Component|Event(s)|
|---|---|
|[Navigation](/help/components/navigation.md)|`cmp:click`|
|[Language Navigation](/help/components/language-navigation.md)|`cmp:click`|
|[Breadcrumb](/help/components/breadcrumb.md)|`cmp:click`|
|[Button](/help/components/button.md)|`cmp:click`|
|[Carousel](/help/components/carousel.md)|`cmp:show` and `cmp:hide`|
|[Tabs](/help/components/tabs.md)|`cmp:show` and `cmp:hide`|
|[Accordion](/help/components/accordion.md)|`cmp:show` and `cmp:hide`|
