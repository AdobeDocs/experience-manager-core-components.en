---
title: Navigation Component
description: The Navigation Component allows users to easily navigate a globalized site structure.
role: Architect, Developer, Admin, User
exl-id: 9154f2a3-3d1e-4865-a413-298748fa66d3
---
# Navigation Component{#navigation-component}

The Navigation Component allows users to easily navigate a globalized site structure.

## Usage {#usage}

The navigation component lists lists a tree of pages so that users of a site can easily navigate the site structure.

The Navigation Component can automatically detect the globalized site structure of your site and [adapt automatically to a localized page.](#localized-site-structure) Additionally it can support any arbitrary site structure by using [shadow redirect pages](#shadow-structure) to represent another structure other than your main content structure.

The [edit dialog](#edit-dialog) allows the content author to define the navigation root page along with the depth of navigation. The [design dialog](#design-dialog) allows the template author to define default values for the navigation root and depth.

## Localized Site Structure Support {#localized-site-structure}

Websites are often provided in multiple languages for different regions. Typically each localized page will contain a navigation element which is included as part of the page template. The Navigation Component allows you to place it once on a template for all pages of your site and it will then adapt automatically for the individual localized pages based on your globalized site structure.

* For an example of how the localization feature of the Navigation Component works, see [the section below](#example-localization).
* For an example of how the localization features of the Core Components work together, see the [Localization Features of the Core Components page](/help/get-started/localization.md).

### Example {#example-localization}

Let's say that your content looks something like this:

```
/content
+-- wknd
   +-- language-masters
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- es
      +-- fr
      \-- it
   +-- us
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      \-- es
   \-- ch
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

For the site WKND, you would probably want to place the Navigation Component on a page template as part of the header. Once part of the template, you can set the **Navigation Root** of the component to `/content/wknd/language-masters/en` since that is where your master content for that site begins. You would maybe also want to set the **Navigation Structure Depth** to be `2` since you probably don't want the entire content tree to be shown by the component, but rather the first two levels so it serves as an overview.

With the **Navigation Root** value, the Navigation Component knows that after `/content/wknd/language-masters/en` that that the navigation begins and it can generate navigation options by recursing the site's structure two levels down (as defined by the **Navigation Structure Depth** value).

No matter what localized page a user is viewing, the Navigation component is able find the corresponding localized page by knowing the location of the current page, working backwards to the root, and then forwards to the corresponding page.

So if a visitor is viewing `/content/ch/de/experience/arctic-surfing-in-lofoten`, the component knows to generate the navigation structure based on `/content/wknd/language-masters/de`. Likewise if the visitor is viewing `/content/us/en/experience/arctic-surfing-in-lofoten`, the component knows to generate the navigation structure based on `/content/wknd/language-masters/en`.

## Shadow Site Structure Support {#shadow-structure}

At times it is necessary to create a navigation menu for the visitor that is different from the actual site structure. Perhaps a promotion should highlight certain content in the menu by rearranging the listing of content. Using shadow pages, which simply redirect to other content pages, the navigation component can generate any arbitrary navigation structure necessary.

To do this you will need to:

1. Create shadow pages as empty pages that represent your desired site structure. This is often referred to as a shadow site structure.
1. Set the **Redirect** values in the page properties on these pages to point to the actual content pages.
1. Set the **Hide in Navigation** option in the page properties of the shadow pages.
1. Set the **Navigation Root** value of the Navigation Component to point to the root of the new shadow site structure.

The Navigation Component will then render the menu based on the shadow site structure. The links rendered by the component are to the actual content pages that the shadow pages redirect to and not to the shadow pages themselves. What's more, the component displays the names of the actual pages as well as correctly highlights the active page, even when the navigation is based on shadow pages. The Navigation Component effectively makes the shadow pages entirely transparent to the visitor.

>[!NOTE]
>Shadow pages make your navigation options much more flexible, but keep in mind that the maintenance of this structure is then completely manual. If you rearrange your actual site content or add/remove content, you will need to manually update your shadow structure as necessary.

>[!NOTE]
>When rendering a shadow site structure, only the shadow pages are recursed by the navigation logic. The logic does not recurse the structure of the redirect destinations.

## Redirects in Navigation {#redirects}

When a page has a redirection target (regardless whether it is pointing to an external URL or to another AEM page), then a navigation component that contains links to that point directly to the URL of the redirection target.

### Example {#redirect-example}

* Create a page A that redirects to page B.
* Create a page C that redirects to `https://aemcomponents.dev`
* On a page D, insert a or navigation component that contains pages A and C
* The respective links that are generated then point directly to page B and `https://aemcomponents.dev`


## Version and Compatibility {#version-and-compatibility}

The current version of the Navigation Component is v1, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM as a Cloud Service|
|--- |--- |--- |---|
|v1|Compatible|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Navigation Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_navigation).

## Technical Details {#technical-details}

The latest technical documentation about the Navigation Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_navigation_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

>[!NOTE]
>
>As of Core Components release 2.1.0, the Navigation Component supports [schema.org microdata](https://schema.org).

## Edit Dialog {#edit-dialog}

In the edit dialog, the content author can define the root page for navigation and the depth of the navigation structure.

### Properties Tab {#properties-tab}

![Navigation Component's edit dialog properties tab](/help/assets/navigation-edit-properties.png)

* **Navigation Root** - The root page, which will be used to generate the navigation tree.
* **Exclude Root Levels** - Often the root should not be included in the navigation. This option allows you to specify how many levels up from the root you wish to exclude. For example:
  * 0 = show the root level
  * 1 = exclude the root level
  * 2 = exclude the root and 1 more level up
  * etc.
* **Collect all child pages** - Collect all pages that are descendants of the navigation root.  
* **Navigation Structure Depth** - Defines how many levels down the navigation tree the component should display relative to the navigation root (only available when **Collect all child pages** is not selected).
* **Disable shadowing** - If the page in the hierarchy is a redirect, the name of the redirecting page will be shown instead of the target. See the [Shadow Site Structure Support](#shadow-structure) for more information.
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

### Accessibility Tab {#accessibility-tab}

![Navigation Component's edit dialog accessibility tab](/help/assets/navigation-edit-accessibility.png)

On the **Accessibility** tab, values can be set for [ARIA accessibility](https://www.w3.org/WAI/standards-guidelines/aria/) labels for the component.

* **Label** - Value of an ARIA label attribute for the component

## Design Dialog {#design-dialog}

The design dialog allows the template author to set the default values for the navigation root page and navigation depth that are presented to the content authors.

### Properties Tab {#properties-tab-design}

![Navigation Component's design dialog](/help/assets/navigation-design.png)

* **Navigation Root** - The default value of the root page of the navigation structure, which will be used to generate the navigation tree and defaulted when the content author adds the component to the page.  
* **Exclude Root Levels** - Often the root should not be included in the navigation. This option allows you to specify the default of how many levels up from the root you wish to exclude. For example:
  * 0 = show the root level
  * 1 = exclude the root level
  * 2 = exclude the root and 1 more level up
  * etc.
* **Collect all child pages** - The default value of the option to collect all pages that are descendants of the navigation root.  
* **Navigation Structure Depth** - The default value of the navigation structure depth.
* **Disable shadowing** - The default value of if shadowing should be disabled when adding a navigation component

### Styles Tab {#styles-tab}

The Navigation Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

The Navigation Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
