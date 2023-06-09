---
title: Email Experience Fragment Component
description: The Email Experience Fragment Component allows the content author to place an Experience Fragment variation in their content while supporting a localized content structure.
role: Architect, Developer, Admin, User
exl-id: 861c1fd1-6d6d-426c-a338-a558326fe16e
---

# Email Experience Fragment Component {#email-experience-fragment-component}

The Email Experience Fragment Component allows the content author to place an Experience Fragment variation in their content while supporting a localized content structure.

## Usage {#usage}

The Email Experience Fragment Component allows the content author to select from existing Experience Fragment variations and place one within the content. An Experience Fragment is a group of content that includes both content and layout and is reusable across channels.

* The component's properties can be defined in the [configure dialog](#configure-dialog).
* Defaults for the component when adding it to content can be defined in the [design dialog](#design-dialog).

The Email Experience Fragment component supports a localized site structure.

## Version and Compatibility {#version-and-compatibility}

The current version of the Email Experience Fragment Component is v1, which was introduced with release X of the Email Core Components in October 2022, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.5|AEM as a Cloud Service|
|---|---|---|
|v1|Compatible|-|

For more information about the Email Core Component versions and releases, see the document [Email Core Components Versions.](/help/email/versions.md)

## Localized Site Structure Support {#localized-site-structure}

The Email Experience Fragment Component is adaptive to localized content structures and renders the proper Experience Fragment based on the localization of the content. To do this, the Experience Fragment must meet the following conditions.

* The Email Experience Fragment Component is added to a [page template.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/templates.html)
* That template is used to create a new content page that is part of a localized structure below `/content/<site>`.
* The Experience Fragment referenced on a content page is part of a localized Experience Fragment structure below `/content/experience-fragments` that follows the same patterns as the site below `/content/<site>` including using the same component names.

In this case, the fragment with the same localization ([language, blueprint, or live copy](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/reusing-content/msm-and-translation.html)) as the current page will be rendered as part of the template.

This behavior is limited to Email Experience Fragment Components added to templates. Experience Fragment Components added to individual content pages will render the exact Experience Fragment renditions configured within the component.

* For an example of how the localization features of the Experience Fragment Component work, see [the section below](#example).
* For an example of how the localization features of the Core Components work together, see the [Localization Features of the Core Components page](/help/get-started/localization.md).

### Example {#example}

Let's say that your content looks something like this:

```
/content
+-- experience-fragments
   \-- wknd
      +-- language-masters
      +-- us
         +-- en
            +-- footerTextXf
            \-- headerTextXf
         \-- es
            +-- footerTextXf
            \-- headerTextXf
      \-- ch
         +-- de
            +-- footerTextXf
            \-- headerTextXf
         +-- fr
            +-- footerTextXf
            \-- headerTextXf
         \-- it
            +-- footerTextXf
            \-- headerTextXf
+-- wknd
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Notice that the structure below `/content/experience-fragments/wknd` mirrors the structure of `/content/wknd`.

In this case, if the Email Experience Fragment component `/content/experience-fragments/wknd/us/en/footerTextXf` is placed on a template, the localized pages created based on that template will automatically render the localized Experience Fragment that corresponds to the localized content page.

So if you navigate to a content page under `/content/wknd/ch/de` that uses the same template, `/content/experience-fragments/wknd/ch/de/footerTextXf` will be rendered instead of `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Fallback {#fallback}

The Email Experience Fragment Component will attempt to find a corresponding localized component in the following order.

1. First it tries to find a language root.
1. If not found, it tries to find a blueprint.
1. If not found, it tries to find a live copy.
1. If not found, it defaults to the Experience Fragment configured in the component.

## Technical Details {#technical-details}

Read the latest [technical documentation about the Experience Fragment Component](https://www.adobe.com/go/aem_cmp_xf_v1).

Further details about developing the Core Components can be found in the [Core Components developer documentation.](/help/developing/overview.md)

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to select the Experience Fragment variation that should be rendered in the content.

![Email Experience Fragment Component's edit dialog](/help/email/assets/email-experience-fragment-edit.png)

Use the **Open Selection Dialog** button to open the component selector to choose which Experience Fragment component variation to add to the content page.

If you add the Email Experience Fragment Component to a template, it will be automatically localized provided that the Experience Fragments are localized, so what is rendered on the page may vary from the component you explicitly select. [See the example above](#example) for more information.

You can also define an **ID**. This option allows controlling the unique identifier of the component in the HTM.

* If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting content.
* If an ID is specified, it is the responsibility of the author to make sure that it is unique.
* Changing the ID can have an impact on CSS.

### Styles Tab {#styles-tab-edit}

The Email Experience Fragment Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling)

Use the drop-down to select the styles that you want to apply to the component. Selections made in the edit dialog have the same effect as those chosen from the component toolbar.

Styles must be configured for this component in the [design dialog](#design-dialog) in order for the tab to be available.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the options available to the content author who uses the Email Experience Fragment Component and the defaults set when placing the Email Experience Fragment Component.

### Styles Tab {#styles-tab}

The Email Experience Fragment Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling)
