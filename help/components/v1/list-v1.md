---
title: List Component (v1)
description: The Core Component List Component allows for the easy creation of dynamic as well as static lists.
index: n
role: Architect, Developer, Administrator, Business Practitioner
---

# List Component (v1) {#list-component-v}

The Core Component List Component allows for the easy creation of dynamic as well as static lists.

## Usage {#usage}

The List Component can be used to create for example a dynamic list of child pages or a static list of arbitrarily defined items.

The type of lists available and formatting options can be defined by the template author in the [design dialog](#design-dialog). The content editor can select from available list types and how to format the list elements in the [edit dialog](#edit-dialog).

## Version and Compatibility {#version-and-compatibility}

This document describes v1 of the List Component, originally introduced with release 1.0.0 of the Core Components with AEM 6.3.

The following table lists the compatibility of v1 of the List Component.

|AEM Version|List Component v1|
|--- |--- |
|6.3|Compatible|
|6.4|Compatible|

>[!CAUTION]
>
>This document describes v1 of the List Component.
>
>For details of the current version of the List Component, see the [List Component](/help/components/list.md) document.

## Sample Component Output {#sample-component-output}

The following is sample taken from [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](/help/assets/chlimage_1-47.png) 

### HTML {#html}

```
<div class="cmp cmp-list aem-GridColumn aem-GridColumn--default--12">

<ul>
    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/arctic-surfing-in-lofoten.html">
            <span class="cmp-list--item-title">Arctic Surfing In Lofoten</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/summit-success-in-the-himalayas.html">
            <span class="cmp-list--item-title">Summit Success in the Himalayas</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/climbing-on-kalymnos-island--greece.html">
            <span class="cmp-list--item-title">Climbing on Kalymnos Island, Greece</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/running-at-the-great-wall-marathon.html">
            <span class="cmp-list--item-title">Running at the Great Wall Marathon</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/skiing-deep-powder-in-siberia.html">
            <span class="cmp-list--item-title">Skiing deep powder in Siberia</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/climbing-in-the-massif-du-mont-blanc.html">
            <span class="cmp-list--item-title">Climbing in the Massif du Mont Blanc</span>
            
        </a>
        
    </article>
</li>
</ul>

</div>
```

### JSON {#json}

```
"articles_list": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/articleslist",
              "tagsMatch": "any",
              "displayAs": "teaser",
              "feedEnabled": "true",
              "listFrom": "children",
              "limit": "0",
              "orderBy": "cq:lastModified",
              "pageMax": "0"
            }
```

>[!NOTE]
>
>JSON export from the Core Components requires release 1.1.0 of the Core Components. Please see the [compatibility information for Core Components v1](/help/versions.md) for more information.

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to configure the list and the list elements.

### List Settings {#list-settings}

The list can be built in different ways.

* [Child pages](#child-pages)
* [Fixed list](#fixed-list)
* [Search](#search-list)
* [Tags](#tags)

Regardless of how the list is built, there are [Sort Options](#sort-options) that can always be configured.

![](/help/assets/chlimage_1-38.png)

Depending on how the content author chooses to build the list, the additional configuration options will change.

#### Child Pages {#child-pages}

The list can be built of the child pages of the current page or another page.

![](/help/assets/chlimage_1-39.png)

* **Parent page**
  * The page whose child pages should make the list
  * Leave blank to use the current page
* **Child-Depth** - How many levels down in the hierarchy should be used

#### Fixed List {#fixed-list}

The list can be built using a fixed list of items.

![](/help/assets/chlimage_1-40.png)

Tap or click the **Add** button to inset a new item to the list.

* Enter text for the item in the list or use the **Selection Dialog** to choose an item from AEM.
* Use the drag handle to re-arrange the items in the list.
* Use the trash can icon to delete items in the list.

#### Search {#search-list}

The list can be built using the results of a search of AEM content.

![](/help/assets/chlimage_1-41.png)

* **Search query** - The string for which a full-text search will be run to generate the list elements
* **Search in** - Where the search should be run
  * Use the **Selection Dialog** to choose the location in AEM
  * Use current page if left blank

#### Tags {#tags}

The list can be built using pages that match certain tags under a particular location.

![](/help/assets/chlimage_1-42.png)

* **Parent page** - Where the tag matching should start
  * Use the **Selection Dialog** to choose the location in AEM
  * Use current page if left blank
* **Tags** - Which tags should be matched
  * Use the **Browse** dialog to select the tags
* **Match** - Define which kind of match should qualify a page to be included in the list
  * **any tag**
  * **all tags**

#### Sort Options {#sort-options}

Regardless of how you choose to build the list, there are certain sorting options that can always be defined.

![](/help/assets/chlimage_1-43.png)

* **Order by** - How the elements should be ordered
  * **Title**
  * **Last modified date**
* **Sort Order** - The order in which the items should be ordered
  * **ascending**
  * **descending**
* **Max Items** - Maximum number of items displayed in list.
  * Leave empty to return all items.

### Item Settings {#item-settings}

Using the **Item Settings** tab, the formatting of the list elements can be configured.

![](/help/assets/chlimage_1-44.png)

* **Link Items**
  Link items to the corresponding page
* **Show Description**
  Show descriptions of the link item
* **Show Date**
  Show modification date of the link item

## Design Dialog {#design-dialog}

The design dialog allows the template author to define what types of lists should be allowed to the content authors as well as the available item settings.

### List Settings {#list-settings-1}

On the **List Settings** tab, the date format can be defined as well as what type of lists should be available in the component to the content authors.

![](/help/assets/chlimage_1-45.png)

* **Date Format** - Format to use for the display of the last modification date
* **Disable Children** - Disable the children list type in the component
* **Disable Static** - Disable the static list type in the component
* **Disable Search** - Disable the search list type in the component
* **Disable Tags** - Disable tags list type in the component

### Item Settings {#item-settings-1}

On the **Item Settings** tab, the formatting options for the individual list elements that should be available in the component for the content authors can be defined.

![](/help/assets/chlimage_1-46.png)

* **Link Items** - Enable Link Items option in the [edit dialog](#edit-dialog)
* **Show Descriptions** - Enable Show Descriptions option in the [edit dialog](#edit-dialog)
* **Show Date** - Enable Show Date option in the [edit dialog](#edit-dialog)

## Technical Details {#technical-details}

The latest technical documentation about the List Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list).

The entire core components project can be downloaded from GitHub.

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).
