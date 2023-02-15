---
title: List Component
description: The Core Component List Component allows for the easy creation of dynamic as well as static lists.
role: Architect, Developer, Admin, User
exl-id: 662ab508-0253-4d28-b95c-8c4cde8173bd
---
# List Component{#list-component}

The Core Component List Component allows for the easy creation of dynamic as well as static lists.

## Usage {#usage}

The List Component can be used to create for example a dynamic list of child pages or a static list of arbitrarily defined items. The type of lists available and formatting options can be defined by the template author in the [design dialog](#design-dialog). The content editor can select from available list types and how to format the list elements in the [edit dialog](#edit-dialog).

## Version and Compatibility {#version-and-compatibility}

The current version of the List Component is v4, which was introduced with release 2.22.0 of the Core Components in February 2023, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM as a Cloud Service|
|--- |--- |--- |---|
|v4|-|Compatible|Compatible|
|[v3](/help/components/v3/list.md)|-|Compatible|Compatible|
|[v2](/help/components/v2/list.md)|Compatible|Compatible|Compatible|
|[v1](/help/components/v1/list-v1.md)|Compatible|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Redirects in Lists {#redirects}

When a page has a redirection target (regardless whether it is pointing to an external URL or to another AEM page), then a list that contains links to that point directly to the URL of the redirection target.

### Example {#redirect-example}

* Create a page A that redirects to page B.
* Create a page C that redirects to `https://aemcomponents.dev`
* On a page D, insert a list component that contains pages A and C
* The respective links that are generated then point directly to page B and `https://aemcomponents.dev`

## Sample Component Output {#sample-component-output}

To experience the List Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_list).

### Technical Details {#technical-details}

The latest technical documentation about the List Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_list_v3).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to configure the list and the list items.

### List Settings Tab {#list-settings-tab}

The list can be built in different ways.

* [Child pages](#child-pages)
* [Fixed list](#fixed-list)
* [Search](#search-options)
* [Tags](#tags)

Regardless of how the list is built, there are [Sort and ID Options](#sort-options) that can always be configured.

![List Component's edit dialog](/help/assets/list-edit.png)

Depending on how the content author chooses to build the list, the additional configuration options will change.

#### Child Pages {#child-pages}

The list can be built of the child pages of the current page or another page.

![Child page options](/help/assets/list-edit-child-pages.png)

* **Parent page**
  * The page whose child pages should make the list
  * Leave blank to use the current page

* **Child-Depth**
  How many levels down in the hierarchy should be used

#### Fixed List {#fixed-list}

The list can be built using a fixed list of items.

![Fixed list options](/help/assets/list-edit-fixed.png)

Tap or click the **Add** button to inset a new item to the list.

* In the **Link** field enter either
  * A fully-qualified URL
  * A relative URL to existing AEM content
    * You can use the **Selection Dialog** to choose an item from AEM.
* In the **Text** field, enter the text that will display for the link in the list.
* Check the checkbox if the link should open in a new browser tab

Once more than one item is created for the list you can arrange the list.

* Use the drag handle to re-arrange the items in the list.
* Use the trash can icon to delete items in the list.

#### Search {#search-options}

The list can be built using the results of a search of AEM content.

![Search list options](/help/assets/list-edit-search.png)

* **Search query**
  The string for which a full-text search will be run to generate the list elements
* **Search in**
  Where the search should be run
  * Use the **Selection Dialog** to choose the location in AEM
  * Use current page if left blank

#### Tags {#tags}

The list can be built using pages that match certain tags under a particular location.

![Tags list options](/help/assets/list-edit-tags.png)

* **Parent page**
  Where the tag matching should start
  * Use the **Selection Dialog** to choose the location in AEM
  * Use current page if left blank
* **Tags**
  Which tags should be matched
  * Use the **Browse** dialog to select the tags
* **Match**
  Define which kind of match should qualify a page to be included in the list
  * **any tag**
  * **all tags**

#### Sort Options {#sort-options}

Regardless of how you choose to build the list, there are certain sorting options that can always be defined.

![Sort options](/help/assets/list-edit-sort-options.png)

* **Order by**
  How the elements should be ordered
  * **Title**
  * **Last modified date**
* **Sort Order**
  The order in which the items should be ordered
  * **ascending**
  * **descending**
* **Max Items**
  Maximum number of items displayed in list.
  * Leave empty to return all items.
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

### Item Settings Tab {#item-settings-tab}

Using the Item Settings tab, the formatting of the list elements can be configured.

![Item settings](/help/assets/list-edit-item-settings.png)

* **Link Items** - Link items to the corresponding page
* **Show Description** - Show descriptions of the link item
* **Show Date** - Show modification date of the link item
* **Display as teaser** - When checked, the item is displayed as a teaser

### Styles Tab {#styles-tab-edit}

The List Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling).

Use the drop-down to select the styles that you want to apply to the component. Selections made in the edit dialog have the same effect as those chosen from the component toolbar.

Styles must be configured for this component in the [design dialog](#design-dialog) in order for the drop down menu to be available.

![Styles tab of the edit dialog of List Component](/help/assets/list-edit-styles.png)

## Design Dialog {#design-dialog}

The design dialog allows the template author to define what types of lists should be allowed to the content authors as well as the available item settings.

### List Settings {#list-settings}

On the **List Settings** tab, the date format can be defined as well as what type of lists should be available in the component to the content authors.

![List Component's design dialog list setting](/help/assets/list-design-list-settings.png)

* **Date Format**
  Format to use for the display of the last modification date
* **Disable children**
  Disable the children list type in the component
* **Disable static**
  Disable the static list type in the component
* **Disable search**
  Disable the search list type in the component
* **Disable tags**
  Disable tags list type in the component

### Item Settings {#item-settings}

On the **Item Settings** tab, the formatting options for the individual list elements that should be available in the component for the content authors can be defined.

![List Component's design dialog item settings](/help/assets/list-design-item-settings.png)

* **Link items**
  Enable Link Items option in the [edit dialog](#edit-dialog)
* **Show descriptions**
  Enable Show Descriptions option in the [edit dialog](#edit-dialog)
* **Show date**
  Enable Show Date option in the [edit dialog](#edit-dialog)

### Styles Tab {#styles-tab}

The Image Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

The List Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
