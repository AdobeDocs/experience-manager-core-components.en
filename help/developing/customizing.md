---
title: Customizing Core Components
description: The Core Components implement several patterns that allow easy customization, from simple styling to advanced functionality reuse.
role: Architect, Developer, Administrator
exl-id: ec4b918b-bc70-4d72-ba84-a24556aedb41
---
# Customizing Core Components{#customizing-core-components}

The [Core Components](overview.md) implement several patterns that allow easy customization, from simple styling to advanced functionality reuse.

## Flexible Architecture {#flexible-architecture}

The Core Components were designed from the beginning to be flexible and extensible. A look at an overview of their architecture reveals where customizations can be made.

![Core Components Architecture](/help/assets/screen_shot_2018-12-07at093742.png)

* [The design dialog](/help/get-started/authoring.md#edit-and-design-dialogs) defines what authors can or cannot do in the edit dialog.
* [The edit dialog](/help/get-started/authoring.md#edit-and-design-dialogs) shows authors only the options they are allowed to use.
* [The Sling model](#customizing-the-logic-of-a-core-component) verifies and prepares the content for the view (template).
* [The result of the Sling model](#customizing-the-logic-of-a-core-component) can be serialized to JSON for SPA use-cases.
* [The HTL renders the HTML](#customizing-the-markup) server-side for traditional server-side rendering.
* [The HTML output](#customizing-the-markup) is semantic, accessible, search-engine optimized, and easy to style.

And all core components implement the [Style System](#styling-the-components).

## AEM Project Archetype {#aem-project-archetype}

[The AEM Project Archetype](/help/developing/archetype/overview.md) creates a minimal Adobe Experience Manager project as a starting point for your own projects, including an example of custom HTL component with SlingModels for the logic and proper implementation of the Core Components with the recommended proxy pattern.

## Customization Patterns {#customization-patterns}

### Customizing Dialogs {#customizing-dialogs}

It may be desired to customize the configuration options available in a core component dialog, be it the [Design Dialog or the Edit Dialog](/help/get-started/authoring.md).

Each dialog has a consistent node structure. It is recommended that this structure is replicated in an inheriting component so that [Sling Resource Merger](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) and [Hide Conditions](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/hide-conditions.html) can be used to hide, replace, or reorder sections of the original dialog. The structure to replicate is defined as anything up to the tab item node level.

To be fully compatible with any changes made to a dialog on its current version, it is very important that structures below the tab item level not be touched (hidden, added to, replaced, reordered, etc.). Instead, a tab item from the parent should be hidden via the `sling:hideResource` property (see [Sling Resource Merger Properties](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/sling-resource-merger.html)), and new tab items added that contain the bespoke configuration fields. `sling:orderBefore` can be used to reorder tab items if necessary.

The dialog below demonstrates the recommended dialog structure as well as how to hide and replace an inherited tab as described above:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<jcr:root xmlns:sling="https://sling.apache.org/jcr/sling/1.0"
          xmlns:jcr="https://www.jcp.org/jcr/1.0"
          xmlns:nt="https://www.jcp.org/jcr/nt/1.0"
          xmlns:granite="https://www.adobe.com/jcr/granite/1.0"
          jcr:primaryType="nt:unstructured">
    <content jcr:primaryType="nt:unstructured">
        <items jcr:primaryType="nt:unstructured">
            <tabs jcr:primaryType="nt:unstructured">
                <items jcr:primaryType="nt:unstructured">
                        <originalTab
                                jcr:primaryType="nt:unstructured"
                                sling:hideResource="true"/>
                        </originalTab>
                        <myTab
                               jcr:primaryType="nt:unstructured"
                               jcr:title="My Tab"
                               sling:resourceType="granite/ui/components/coral/foundation/container"/>
                               <!-- myTab content -->
                        </myTab>
                </items>
            </basic>
        </items>
    </content>
</jcr:root>
```

### Customizing the Logic of a Core Component {#customizing-the-logic-of-a-core-component}

The Business logic for the core components is implemented in Sling Models. This logic can be extended by using a Sling delegation pattern.

For example, the title core component uses the `jcr:title` property of the requested resource to provide the title text. If no `jcr:title` property is defined, a fallback to the current page title is implemented. We want to change the behavior so that the title of the current page is always displayed.

Because the implementation of the Core Components' models are private, they must be extended with a delegation pattern.

```java
@Model(adaptables = SlingHttpServletRequest.class,
       adapters = Title.class,
       resourceType = "myproject/components/pageHeadline")
public class PageHeadline implements Title {
    @ScriptVariable private Page currentPage;
    @Self @Via(type = ResourceSuperType.class)
    private Title title;
    @Override public String getText() {
        return currentPage.getTitle();
    }
    @Override public String getType() {
        return title.getType();
    }
}
```

For further details about the delegation pattern see the Core Components GitHub Wiki article [Delegation Pattern for Sling Models](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models).

### Customizing the Markup {#customizing-the-markup}

Sometimes advanced styling requires a different markup structure of the component.

This can easily be done by copying the HTL files that need to be modified from the Core Component into the [proxy component.](guidelines.md#proxy-component-pattern)

Taking again the example of the Core Breadcrumb Component, to customize its markup output, the `breadcrumb.html` file would have to be copied into the site-specific component that has a `sling:resourceSuperTypes` that points to the Core Breadcrumb Component.

### Styling the Components {#styling-the-components}

The first form of customization is to apply CSS styles.

To make this easy, the Core Components render semantic markup and follow a standardized naming convention inspired by [Bootstrap](https://getbootstrap.com/). Also, to easily target and namespace the styles for the individual components, each Core Component is wrapped in a DIV element with the " `cmp`" and " `cmp-<name>`" classes.

For instance, looking at the HTL file of the v1 Core Breadcrumb Component: [breadcrumb.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html), we see that the hierarchy of elements output are `ol.breadcrumb > li.breadcrumb-item > a`. So to make sure that a CSS rule only affects the breadcrumb class of that component, all rules should be namespaced as shown below:

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

Additionally, each of the Core Components leverage the AEM [Style System feature](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html) that allows template authors to define additional CSS class names that can be applied to the component by the page authors. This allows to define for each template a list of allowed component styles, and whether one of them should apply by default to all components of that kind.

## Upgrade Compatibility of Customizations {#upgrade-compatibility-of-customizations}

Three different kind of upgrades are possible:

* upgrading the version of AEM
* upgrading the Core Components to a new minor version
* upgrading the Core Components to a major version

Generally, upgrading AEM to a new version won't impact the Core Components or the customizations done, provided that the components' versions also support the new AEM version that is being migrated to, and that customizations don't use APIs that have been [deprecated or removed](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html).

Upgrading the Core Components without switching to a newer major version shouldn't affect customizations, as long as the customization patterns described on this page are used.

Switching to a newer major version of the Core Components is compatible only for the content structure, but customizations may need to be refactored. Clear change logs will be published for each component version to highlight the changes that would impact the kind of customizations described on this page.

## Support of Customizations {#support-of-customizations}

Like for any AEM component, there are a number of things to be aware of regarding customizations:

1. **Never modify the code of Core Components directly.**
  
   This would make them unsupported entirely, and make future updates of the components a painful process. Instead, use the customization methods described on this page.

1. **Custom code is your own responsibility.**
  
   Our support program doesn't cover custom code, and reported issues that cannot be reproduced with vanilla Core Components that are [used as documented](/help/get-started/using.md) won't qualify.

1. **Watch deprecated and removed functionality.**
  
   With each new AEM version being upgraded to, ensure that all API used are still topical by keeping an eye on the [Deprecated and Removed Features](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html) page.

See also the [Core Component Support](overview.md#core-component-support) section.

**Read next:**

* [Using Core Components](/help/get-started/using.md) - get up-and-running with Core Components in your own project.
* [Component Guidelines](guidelines.md) - to learn the implementation patterns of the Core Components.
