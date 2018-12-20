---
title: Tabs Component
seo-title: Tabs Component
description: The Tabs Component allows the creation of multiple tabs to arrange content on a page.
seo-description: The Tabs Component allows the creation of multiple tabs to arrange content on a page.
uuid: 46f71233-8b12-4887-a0c6-ad24dc469cb1
content-type: reference
topic-tags: authoring
topic-tags: core-components
discoiquuid: 966d47fb-d35d-4103-b29d-4ef0aa739f24
---

# Tabs Component{#tabs-component}

The Core Component Tabs Component allows organization of content onto multiple tabs.

## Usage {#usage}

The Tabs Component allows the content author to organize page content within multiple tabs.

The [edit dialog](tabs.md#main-pars_title) allows the content author to define multiple tabs as well as set the active tab. Using the [design dialog](tabs.md#main-pars_title_1995166862), the template author can define which components can be added to tabs and customize the styles.

>[!NOTE]
>
>Nested tab components (tabs within tabs) are supported.
>
>Simple (non-nested) tab components can be located/selected using the [content tree](/content/help/en/experience-manager/6-4/sites/authoring/using/author-environment-tools#main-pars_title_96d3), however nested tabs can not be.

## Version and Compatibility {#version-and-compatibility}

The current version of the Tabs Component is v1, which was introduced with release 2.2.0 of the Core Components in October 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.3|AEM 6.4|
|--- |--- |--- |
|v1|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

The following is a sample taken from [We.Retail](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](assets/screenshot_2018-11-28at142504.png) 

### HTML {#html}

```
<div class="cmp-tabs">
    <ol role="tablist" class="cmp-tabs__tablist" aria-multiselectable="false">
        <li role="tab" class="cmp-tabs__tab" data-cmp-hook-tabs="tab" aria-selected="false" tabindex="-1">Text Tab</li>
<li role="tab" class="cmp-tabs__tab cmp-tabs__tab--active" data-cmp-hook-tabs="tab" aria-selected="true" tabindex="0">Image Tab</li>

    </ol>
    <div role="tabpanel" class="cmp-tabs__tabpanel" data-cmp-hook-tabs="tabpanel" aria-hidden="true"><div class="responsivegrid">

<div class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
    
    <div class="text aem-GridColumn aem-GridColumn--default--12">
<div class="cmp-text">
    <p>This tab is dedicated to extolling the virtue of toast as the finest food known to man.</p>

</div>

</div>
    
</div></div>
</div>
<div role="tabpanel" class="cmp-tabs__tabpanel cmp-tabs__tabpanel--active" data-cmp-hook-tabs="tabpanel"><div class="responsivegrid">

<div class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
    
    <div class="image aem-GridColumn aem-GridColumn--default--12">
<div data-cmp-src="/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/tabs/item_2/image.coreimg.82{.width}.jpeg/1543411469819.jpeg" data-cmp-widths="128,256,512,1024,1280,1440,1920,2048" data-asset="/content/dam/we-retail/en/products/activities/surfing/source/Bear Bottom.jpg" data-asset-id="a5fcd1e7-5c52-4480-98cb-d962b079d862" class="cmp-image" itemscope="" itemtype="https://schema.org/ImageObject">
    
        <img class="cmp-image__image" itemprop="contentUrl" data-cmp-hook-image="image" alt="" src="/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/tabs/item_2/image.coreimg.82.1024.jpeg/1543411469819.jpeg">
 
</div>
    
</div>
    
</div></div>
</div>
    
</div>
```

### JSON {#json}

```
"tabs": {
              ":itemsOrder": [
                "item_1",
                "item_2"
              ],
              ":type": "weretail/components/content/tabs",
              ":items": {
                "item_1": {
                  "columnCount": 12,
                  "columnClassNames": {
                    "text": "aem-GridColumn aem-GridColumn--default--12"
                  },
                  "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
                  ":items": {
                    "text": {
                      "text": "<p>This tab is dedicated to extolling the virtue of toast as the finest food known to man.</p>\n",
                      "richText": true,
                      ":type": "weretail/components/content/text"
                    }
                  },
                  ":itemsOrder": [
                    "text"
                  ],
                  ":type": "wcm/foundation/components/responsivegrid",
                  "cq:panelTitle": "Text Tab"
                },
                "item_2": {
                  "columnCount": 12,
                  "columnClassNames": {
                    "image": "aem-GridColumn aem-GridColumn--default--12"
                  },
                  "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
                  ":items": {
                    "image": {
                      "src": "/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/tabs/item_2/image.coreimg.jpeg/1543411469819.jpeg",
                      "srcUriTemplate": "/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/tabs/item_2/image.coreimg.82{.width}.jpeg/1543411469819.jpeg",
                      "areas": [],
                      "uuid": "a5fcd1e7-5c52-4480-98cb-d962b079d862",
                      "widths": [
                        128,
                        256,
                        512,
                        1024,
                        1280,
                        1440,
                        1920,
                        2048
                      ],
                      "lazyEnabled": false,
                      ":type": "weretail/components/content/image"
                    }
                  },
                  ":itemsOrder": [
                    "image"
                  ],
                  ":type": "wcm/foundation/components/responsivegrid",
                  "cq:panelTitle": "Image Tab"
                }
              }
            }
```

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to create, rename, and rearrange tabs as well as define the active tab.

### Items Tab {#items-tab}

![](assets/screenshot_2018-10-11at153557.png)

Use the **Add** button to open the component selector to choose which component to add as a tab. Once added, an entry is added to the list, which contains the following columns:

* **Icon**
  The icon of the component type of the tab for easy identification in the list. Mouse over to see the full component name as a tooltip.
* **Description**
  The description used as the text of the tab, defaulting to the name of the component selected for the tab.
* **Delete**
  Tap or click to delete the tab from the tab component.
* **Rearrange**
  Tap or click and drag to rearrange the order of the tabs.

### Properties Tab {#properties-tab}

![](assets/screenshot_2018-10-19at140646.png)

On the **Properties** tab, the content author can define which tab is active when the page is loaded. With the **Default** option, the first tab will be selected.

## Select Panel {#select-panel}

The content author can use the **Select Panel** option on the component toolbar to change to a different panel for editing as well as to easily rearrange the order of the tabs.

![](assets/screenshot_2018-10-11at165417.png)

Once selecting the **Select Panel** option in the component toolbar, the configured tabs are displayed as a drop-down.

* The list is ordered by the assigned arrangement of the tabs and is reflected in the numbering.
* The component type of the tab is displayed first, followed by the description of the tab in lighter font.

![](assets/screenshot_2018-10-11at165154.png)

* Tapping or clicking an entry in the dropdown, switches the view in the editor to that tab.
* The tabs can be rearranged in-place by using the drag handles.

>[!NOTE]
>
>Tabs are not selectable by the author when in **Edit** mode. Use [**Preview** mode](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/editing-content.html#main-pars_title_196884421) or the ** [View as Published](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/editing-content.html#main-pars_title_1534569976)** option to interact with the tabs as a reader of the published content would.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define which components can be added as items to the tabs component as well as define which custom styles are available to the content author.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to the tabs component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/template.html#main-pars_procedure_1914319072)

### Styles Tab {#styles-tab}

The Tabs Component supports the AEM [Style System](authoring.md#main-pars_header).

## Technical Details {#technical-details}

The latest technical documentation about the Tabs Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/tabs/v1/tabs).

The entire core components project can be downloaded from GitHub.

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md). 
