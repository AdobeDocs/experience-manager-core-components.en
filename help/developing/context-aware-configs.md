---
title: Sling Context-Aware Configurations and Core Components
description: The Core Components leverage Sling context-aware configurations for certain features
role: Developer, Admin
exl-id: d35210f7-a65d-4768-ab9e-f12ec406da2d
TQID: https://experienceleague.adobe.com/jCBeHjuqLJzIxggeZxpusUkv9ZAyE-Ktr5N-gakWK18
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Sling Context-Aware Configurations and Core Components {#sling-context-aware-configurations}

Context-aware configurations are a [feature of Sling](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html). They are configurations that are related to a content resource or a resource tree and are leveraged by the Core Components to allow site-wide configurations.

## Sling Context-Aware Configurations {#context-aware-configurations}

Your site may need different configurations for different sites regions for instance where some parameters may be shared requiring inheritance for nested contexts and global fallback values. AEM leverages Sling context aware configurations, which enable this possibility.

For details about configurations in AEM, [see the Configurations and Configuration Browser documentation.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/configurations.html)

## Use in the Core Components {#core-components}

A number of Core Components features leverage context-aware configurations. All such configurations are located under the following node:

* `/conf/<my-site>/sling:configs/<my-configuration>`

Individual configurations depend on the specific component or feature. Features of the Core Components that use context-aware configurations include:

* [The Page Component](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/page/v3/page#loading-of-context-aware-cssjs) relies on context-aware configuration when rendering `link`, `script` and `meta` tags.
* [PDF Viewer Component](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Adobe Client Data Layer](/help/developing/data-layer/overview.md#installation-activation)
* [AMP Support](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
