---
title: AMP Support for the Core Components
description: The Core Components support AMP - Accelerated Mobile Pages
---

# AMP Support for the Core Components {#amp-support}

As of [release 2.11.0](/help/versions.md) of the Core Components, [AMP - Accelerated Mobile Pages](https://developers.google.com/amp) - are fully supported.

This document gives an overview of how AMP is supported as well as how to enable it for your sites. However for full technical details, please see the [GitHub developer documentation.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## What is AMP? {#what-is-amp}

Accelerated Mobile Pages or AMP is an open-source framework originally designed by Google to optimize pages for mobile browsing. AMP pages typically load much more quickly than standard web pages, offering better mobile experiences.

## AMP in the Core Components {#amp-in-core-components}

Support for AMP in the Core Components is [fully configurable.](#enabling-amp) AMP versions of pages can be served exclusively, alongside the standard HTML versions, or not at all.

The Core Components use `amp` as a Sling selector to render an AMP page. For example `example.html` would render the normal page and `example.amp.html` would be the AMP version.

### Requirements {#requirements}

When using AMP with the Core Components, the main difference is that AMP requires all CSS to be inlined in the `<head>` element as well as optimized.

To support this, a customized page component is used, which loads just the AMP-specific CSS for components present on the page.

For further requirements and technical details, please see the [GitHub developer documentation.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

### Using AMP in the Core Components {#using-amp}

Individual projects can decide whether or not to leverage AMP. In fact, because AMP and standard HTML pages can be delivered in parallel, a project can choose to use AMP on only certain pages of the project.

### Installing AMP Support {#installing-amp}

Because AMP is optional, it is delivered as an extension to the Core Components.

* For AEM as a Cloud Service projects, the extension is automatically available.
* For on-premise and AMS projects, the extension must be explicitly installed when installing the Core Components.

Once the extension is installed, the component author must simply point the component supertypes to those in the extension.

### Enabling AMP for Pages {#enabling-amp}

To enable AMP for a page, the **AMP Mode** must be selected in the [Page Policy.](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/templates.html#editingatemplatepagepolicies)

![AMP Page Policy options](/help/assets/amp-policy.png)

* **No AMP** - The page is delivered as standard HTML only.
* **Paired AMP** - The page is delivered as AMP as well as HTML.
* **AMP Only** - The page is delivered as AMP only.

The AMP settings for a page can also be overridden in the [Page Properties](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/authoring/editing-page-properties.html) for an individual page.

![AMP Page Properties](/help/assets/amp-page-properties.png)

* **Inherit from Page Template** - This is the default value allowing the setting to be taken from the page template's policy.
* **No AMP** - The page is delivered as standard HTML only.
* **Paired AMP** - The page is delivered as AMP as well as HTML.
* **AMP Only** - The page is delivered as AMP only.
