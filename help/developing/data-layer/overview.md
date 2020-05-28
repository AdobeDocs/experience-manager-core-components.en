---
title: Using the Adobe Data Layer with the Core Components
description: Using the Adobe Data Layer with the Core Components
---

# Using the Adobe Data Layer with the Core Components {#data-layer-core-components}

The goal of the Adobe Client Data Layer is to reduce the effort to instrument websites by providing a standardized method to expose and access any kind of data for any script.

The Adobe Data Layer is platform agnostic, but is fully integrated into the Core Components for use with AEM.

Like the Core Components, the code for the Adobe Data Layer is available on GitHub along with its developer documentation. This document gives an overview of how the Core Components interact with the Data Layer, but full technical details are deferred to the GitHub documentation.

## Installion and Activation {#installation-activation}

As of Core Components release 2.9.0, the Data Layer is distributed with the Core Components as a clientlib. No installation is necessary.

However the Data Layer is not activated by default. To activate the Data Layer, a property on a `sling:configs` node must be set.

Under your project create the following node:

`/conf/<yourSite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`

And then add a boolean property called `enabled` set to `true`.

Once enabled, you can verify the activation by loading a page of the site outside of the editor. When you inspect the page you will see that the Adobe Data Layer is loaded.

## Core Components Data Schemas {#data-schemas}

The following is a list of schemas that the Core Components use with the Data Layer.

### Page Schema {#page}

The Page schema is used by the following component:

* [Page](/help/components/page.md)

The Page schema is defined as follows.

```
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    xdm:tags
    repo:path
    xdm:template
    xdm:language
}
```

### Container Schema {#container}

The Container schema is used by the following components:

* [Accordion](/help/components/accordion.md)
* [Tabs](/help/components/tabs.md)
* [Carousel](/help/components/carousel.md)

The Container schema is defined as follows.

```
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    shownItems
}
```

### Image Schema {#image}

The Image schema is used by the following component:

* [Image](/help/components/image.md)

The Image schema is defined as follows.

```
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    image
}
```

### Asset Schema {#asset}

The Asset schema is used inside the [Image component.](/help/components/image.md)

The Asset schema is defined as follows.

```
id: {
    repo:id
    repo:path
    @type
    xdm:tags
    repo:modifyDate
}
```

### Component/Container Item Schema {#item}

The Component/Container Item schema is used inside all other components.

The Component/Container Item schema is defined as follows.

```
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
}
```
