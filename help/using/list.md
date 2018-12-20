---
title: List Component
seo-title: List Component
description: null
seo-description: The Core Component List Component allows for the easy creation of dynamic as well as static lists.
uuid: 50a572e8-b444-4f7d-82bc-5a93ebb4be95
contentOwner: User
content-type: reference
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 89053323-6221-46ed-896a-31a42c55282e
disttype: dist5
gnavtheme: light
groupsectionnavitems: no
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
index: y
internal: n
snippet: y
---

# List Component{#list-component}

The Core Component List Component allows for the easy creation of dynamic as well as static lists.

## Usage {#usage}

The List Component can be used to create for example a dynamic list of child pages or a static list of arbitrarily defined items. The type of lists available and formatting options can be defined by the template author in the [design dialog](list.md#main-pars_title_1995166862). The content editor can select from available list types and how to format the list elements in the [edit dialog](list.md#main-pars_title).

## Version and Compatibility {#version-and-compatibility}

The current version of the List Component is v2, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

<table border="1" cellpadding="1" cellspacing="0" width="100%"> 
 <tbody> 
  <tr> 
   <td>Component Version<br /> </td> 
   <td>AEM 6.3</td> 
   <td>AEM 6.4</td> 
  </tr> 
  <tr> 
   <td>v2<br /> </td> 
   <td>Compatible</td> 
   <td>Compatible</td> 
  </tr> 
  <tr> 
   <td><a href="../using/text-v1.md">v1</a></td> 
   <td>Compatible<a href="../using/list-v1.md"></a></td> 
   <td>Compatible</td> 
  </tr> 
 </tbody> 
</table>

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

The following is sample taken from [We.Retail](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](assets/screen_shot_2018-01-12at105924.png) 

### HTML {#html}

```
<ul class="cmp-list">
    <li class="cmp-list__item">
    <article>
        <a class="cmp-list__item-link" href="/content/we-retail/us/en/experience/arctic-surfing-in-lofoten.html">
            <span class="cmp-list__item-title">Arctic Surfing In Lofoten</span>
            
        </a>
        
    </article>
</li>

    <li class="cmp-list__item">
    <article>
        <a class="cmp-list__item-link" href="/content/we-retail/us/en/experience/summit-success-in-the-himalayas.html">
            <span class="cmp-list__item-title">Summit Success in the Himalayas</span>
            
        </a>
        
    </article>
</li>

    <li class="cmp-list__item">
    <article>
        <a class="cmp-list__item-link" href="/content/we-retail/us/en/experience/climbing-on-kalymnos-island--greece.html">
            <span class="cmp-list__item-title">Climbing on Kalymnos Island, Greece</span>
            
        </a>
        
    </article>
</li>

    <li class="cmp-list__item">
    <article>
        <a class="cmp-list__item-link" href="/content/we-retail/us/en/experience/running-at-the-great-wall-marathon.html">
            <span class="cmp-list__item-title">Running at the Great Wall Marathon</span>
            
        </a>
        
    </article>
</li>

    <li class="cmp-list__item">
    <article>
        <a class="cmp-list__item-link" href="/content/we-retail/us/en/experience/skiing-deep-powder-in-siberia.html">
            <span class="cmp-list__item-title">Skiing deep powder in Siberia</span>
            
        </a>
        
    </article>
</li>

    <li class="cmp-list__item">
    <article>
        <a class="cmp-list__item-link" href="/content/we-retail/us/en/experience/climbing-in-the-massif-du-mont-blanc.html">
            <span class="cmp-list__item-title">Climbing in the Massif du Mont Blanc</span>
            
        </a>
        
    </article>
</li>
</ul>
```

### JSON {#json}

```
"list":{  
                           "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                           "dateFormatString":"yyyy-MM-dd",
                           "items":[  
                              {  
                                 "url":"/content/we-retail/us/en/experience/arctic-surfing-in-lofoten.html",
                                 "path":"/content/we-retail/us/en/experience/arctic-surfing-in-lofoten",
                                 "description":null,
                                 "title":"Arctic Surfing In Lofoten",
                                 "lastModified":1457990337837
                              },
                              {  
                                 "url":"/content/we-retail/us/en/experience/summit-success-in-the-himalayas.html",
                                 "path":"/content/we-retail/us/en/experience/summit-success-in-the-himalayas",
                                 "description":null,
                                 "title":"Summit Success in the Himalayas",
                                 "lastModified":1457990337858
                              },
                              {  
                                 "url":"/content/we-retail/us/en/experience/climbing-on-kalymnos-island--greece.html",
                                 "path":"/content/we-retail/us/en/experience/climbing-on-kalymnos-island--greece",
                                 "description":null,
                                 "title":"Climbing on Kalymnos Island, Greece",
                                 "lastModified":1457990337878
                              },
                              {  
                                 "url":"/content/we-retail/us/en/experience/running-at-the-great-wall-marathon.html",
                                 "path":"/content/we-retail/us/en/experience/running-at-the-great-wall-marathon",
                                 "description":null,
                                 "title":"Running at the Great Wall Marathon",
                                 "lastModified":1457990337900
                              },
                              {  
                                 "url":"/content/we-retail/us/en/experience/skiing-deep-powder-in-siberia.html",
                                 "path":"/content/we-retail/us/en/experience/skiing-deep-powder-in-siberia",
                                 "description":null,
                                 "title":"Skiing deep powder in Siberia",
                                 "lastModified":1457990337920
                              },
                              {  
                                 "url":"/content/we-retail/us/en/experience/climbing-in-the-massif-du-mont-blanc.html",
                                 "path":"/content/we-retail/us/en/experience/climbing-in-the-massif-du-mont-blanc",
                                 "description":null,
                                 "title":"Climbing in the Massif du Mont Blanc",
                                 "lastModified":1457990337942
                              }
                           ],
                           "showDescription":false,
                           "showModificationDate":false,
                           "linkItems":true,
                           ":type":"weretail/components/content/list"
                        }
```

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to configure the list and the list items.

### List Settings Tab {#list-settings-tab}

The list can be built in different ways.

* [Child pages](list.md#main-pars_title_1861279796)
* [Fixed list](list.md#main-pars_title_1227896889)
* [Search](list.md#main-pars_title_1224003560)
* [Tags](list.md#main-pars_title_700759533)

Regardless of how the list is built, there are [Sort Options](list.md#main-pars_title_1568376452) that can always be configured.

![](assets/chlimage_1-38.png)

Depending on how the content author chooses to build the list, the additional configuration options will change.

#### Child Pages {#child-pages}

The list can be built of the child pages of the current page or another page.

![](assets/chlimage_1-39.png)

* **Parent page**

    * The page whose child pages should make the list
    * Leave blank to use the current page

* **Child-Depth** - How many levels down in the hierarchy should be used

#### Fixed List {#fixed-list}

The list can be built using a fixed list of items.

![](assets/chlimage_1-40.png)

Tap or click the **Add** button to inset a new item to the list.

* Enter text for the item in the list or use the **Selection Dialog** to choose an item from AEM.
* Use the drag handle to re-arrange the items in the list.
* Use the trash can icon to delete items in the list.

#### Search {#search}

The list can be built using the results of a search of AEM content.

![](assets/chlimage_1-41.png)

* **Search query** - The string for which a full-text search will be run to generate the list elements
* **Search in** - Where the search should be run

    * Use the **Selection Dialog** to choose the location in AEM
    * Use current page if left blank

#### Tags {#tags}

The list can be built using pages that match certain tags under a particular location.

![](assets/chlimage_1-42.png)

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

![](assets/chlimage_1-43.png)

* **Order by** - How the elements should be ordered

    * **Title**
    * **Last modified date**

* **Sort Order** - The order in which the items should be ordered

    * **ascending**
    * **descending**

* **Max Items** - Maximum number of items displayed in list.

    * Leave empty to return all items.

### Item Settings Tab {#item-settings-tab}

Using the Item Settings tab, the formatting of the list elements can be configured.

![](assets/chlimage_1-44.png)

* **Link Items** - Link items to the corresponding page
* **Show Description** - Show descriptions of the link item
* **Show Date** - Show modification date of the link item

## Design Dialog {#design-dialog}

The design dialog allows the template author to define what types of lists should be allowed to the content authors as well as the available item settings.

### List Settings {#list-settings}

On the **List Settings** tab, the date format can be defined as well as what type of lists should be available in the component to the content authors.

![](assets/chlimage_1-45.png)

* **Date Format **- Format to use for the display of the last modification date
* **Disable Children** - Disable the children list type in the component
* **Disable Static** - Disable the static list type in the component
* **Disable Search** - Disable the search list type in the component
* **Disable Tags** - Disable tags list type in the component

### Item Settings {#item-settings}

On the **Item Settings** tab, the formatting options for the individual list elements that should be available in the component for the content authors can be defined.

![](assets/chlimage_1-46.png)

**Link Items **- Enable Link Items option in the [edit dialog](list.md#main-pars_title_550499279)

**Show Descriptions** - Enable Show Descriptions option in the [edit dialog](list.md#main-pars_title_550499279)

**Show Date **- Enable Show Date option in the [edit dialog](list.md#main-pars_title_550499279)

### Styles Tab {#styles-tab}

The Image Component supports the AEM [Style System](authoring.md#main-pars_header).

## Technical Details {#technical-details}

The latest technical documentation about the List Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list).

The entire core components project can be downloaded from GitHub.

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md). 
