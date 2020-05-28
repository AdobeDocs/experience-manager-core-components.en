---
title: Using the Adobe Data Layer with the Core Components
description: Using the Adobe Data Layer with the Core Components
---

# Using the Adobe Data Layer with the Core Components {#data-layer-core-components}

The goal of the Adobe Client Data Layer is to reduce the effort to instrument websites by providing a standardized method to expose and access any kind of data for any script.

The Adobe Data Layer is platform agnostic, but is fully integrated into the Core Components for use with AEM.

Like the Core Components, the code for the Adobe Data Layer is available on GitHub along with its developer documentation. This document gives an overview of how the Core Components interact with the Data Layer, but full technical details are deferred to the GitHub documentation.

## Installing and Activation {#installation-activation}

As of Core Components release 2.9.0, the Data Layer is distributed with the Core Components as a clientlib. No installation is necessary.

However the Data Layer is not activated by default. To activate the Data Layer, a property on a `sling:configs` node must be set.

Under your project create the following node:

`/conf/<yourSite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`

And then add a boolean property called `enabled` set to `true`.

Once enabled, you can verify the activation by loading a page of the site outside of the editor. When you inspect the page you will see that the Adobe Data Layer is loaded.

