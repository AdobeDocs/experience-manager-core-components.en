---
title: Sling Context-Aware Configurations and Core Components
description: The Core Components leverage Sling context-aware configurations for certain features
---

# Sling Context-Aware Configurations and Core Components {#sling-context-aware-configurations}

Context-aware configurations are a [feature of Sling](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html). They are configurations that are related to a content resource or a resource tree and are leveraged by the Core Components to allow site-wide configurations.

## Sling Context-Aware Configurations {#context-aware-configurations}

Your site may need different configurations for different sites regions for instance where some parameters may be shared requiring inheritance for nested contexts and global fallback values. AEM leverages Sling context aware configurations, which enable this possibility.

For details about configurations in AEM, [see the Configurations and Configuration Browser documentation.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/configurations.html)

## Use in the Core Components {#core-components}

A number of Core Components features leverage context-aware configurations. All such configurations are located under the following node:

* `/conf/<my-site>/sling:configs/<my-configuration>`

Individual configurations depend on the specific component or feature. Features of the Core Components that use context-aware configurations are:

* [PDF Viewer Component](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Adobe Client Data Layer](/help/developing/data-layer/overview.md#installation-activation)
* [AMP Support](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
