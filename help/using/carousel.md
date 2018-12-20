---
title: Carousel Component
seo-title: Carousel Component
description: null
seo-description: The Carousel Component allows the content author to present content in a rotating carousel.
uuid: 34934491-bd85-4f1e-ae22-bb48ed4dbd5c
content-type: reference
topic-tags: authoring
topic-tags: core-components
discoiquuid: 3510812b-9d3e-40fe-b986-0f15d40b42ad
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

# Carousel Component{#carousel-component}

The Core Component Carousel Component allows the content author to present content in a navigable carousel.

## Usage {#usage}

Using the Carousel Component, the content author to organize content in a rotating carousel of slides.

The [edit dialog](carousel.md#main-pars_title) allows the content author to create, name, and order multiple slides as well as enable auto-transition with delay. Using the [design dialog](carousel.md#main-pars_title_1995166862), the template author can define which components can be added to the carousel, enable or disable automatic transitions, and customize the styles.

## Version and Compatibility {#version-and-compatibility}

The current version of the Carousel Component is v1, which was introduced with release 2.2.0 of the Core Components in October 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.3|AEM 6.4|
|--- |--- |--- |
|v1|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

The following is a sample taken from [We.Retail](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](assets/screenshot_2018-11-28at140433.png) 

### HTML {#html}

```
<div class="we-carousel aem-GridColumn aem-GridColumn--default--12">
<div class="cmp-carousel" data-cmp-delay="5000">
    <div class="cmp-carousel__content">
        <div role="tabpanel" class="cmp-carousel__item cmp-carousel__item--active" data-cmp-hook-carousel="item"><div class="image">
<div data-cmp-src="/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/carousel/image_137106943.coreimg.82{.width}.jpeg/1543410175846.jpeg" data-cmp-widths="128,256,512,1024,1280,1440,1920,2048" data-asset="/content/dam/we-retail/en/experiences/arctic-surfing-in-lofoten/northern-lights.jpg" data-asset-id="24be0df2-92ae-4cd5-91f2-ca5a7fbf3dff" data-title="Northern Lights" class="cmp-image" itemscope="" itemtype="https://schema.org/ImageObject">
    
        <img class="cmp-image__image" itemprop="contentUrl" data-cmp-hook-image="image" alt="Arctic Surfing in Lofoten, Northern Norway, Europe" title="Northern Lights" src="/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/carousel/image_137106943.coreimg.82.1024.jpeg/1543410175846.jpeg">
    
    <meta itemprop="caption" content="Northern Lights">
</div>

</div>
</div>
<div role="tabpanel" class="cmp-carousel__item" data-cmp-hook-carousel="item" aria-hidden="true"><div class="image">
<div data-cmp-src="/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/carousel/image_162165685.coreimg.82{.width}.jpeg/1543410196033.jpeg" data-cmp-widths="128,256,512,1024,1280,1440,1920,2048" data-asset="/content/dam/we-retail/en/experiences/arctic-surfing-in-lofoten/surfer-wave-02.jpg" data-asset-id="b55dc097-e0cb-4219-9525-dda1fb64fd8c" data-title="Surfer Wave 02" class="cmp-image" itemscope="" itemtype="https://schema.org/ImageObject">
    
        <img class="cmp-image__image" itemprop="contentUrl" data-cmp-hook-image="image" alt="Arctic Surfing in Lofoten, Northern Norway, Europe" title="Surfer Wave 02" src="/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/carousel/image_162165685.coreimg.82.1024.jpeg/1543410196033.jpeg">
    
    <meta itemprop="caption" content="Surfer Wave 02">
</div>

</div>
</div>
<div role="tabpanel" class="cmp-carousel__item" data-cmp-hook-carousel="item" aria-hidden="true"><div class="image">
<div data-cmp-src="/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/carousel/image.coreimg.82{.width}.jpeg/1543410210981.jpeg" data-cmp-widths="128,256,512,1024,1280,1440,1920,2048" data-asset="/content/dam/we-retail/en/experiences/arctic-surfing-in-lofoten/majestic-rainbow.jpg" data-asset-id="72feab95-6040-4af8-a199-a11a23e22a56" data-title="Majestic Rainbow" class="cmp-image" itemscope="" itemtype="https://schema.org/ImageObject">
    
        <img class="cmp-image__image" itemprop="contentUrl" data-cmp-hook-image="image" alt="Arctic Surfing in Lofoten, Northern Norway, Europe" title="Majestic Rainbow" src="/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/carousel/image.coreimg.82.1024.jpeg/1543410210981.jpeg">
    
    <meta itemprop="caption" content="Majestic Rainbow">
</div>

</div>
</div>

        <button role="button" class="cmp-carousel__action cmp-carousel__action--previous" data-cmp-hook-carousel="previous">
            <span class="cmp-carousel__action-icon"></span>
            <span class="cmp-carousel__action-text">Previous</span>
        </button>
        <button role="button" class="cmp-carousel__action cmp-carousel__action--next" data-cmp-hook-carousel="next">
            <span class="cmp-carousel__action-icon"></span>
            <span class="cmp-carousel__action-text">Next</span>
        </button>
        
        <ol role="tablist" class="cmp-carousel__indicators" data-cmp-hook-carousel="indicators">
            <li role="tab" class="cmp-carousel__indicator cmp-carousel__indicator--active" data-cmp-hook-carousel="indicator" aria-selected="true" tabindex="0">Northern Lights</li>
<li role="tab" class="cmp-carousel__indicator" data-cmp-hook-carousel="indicator" aria-selected="false" tabindex="-1">Mad-crazy waves</li>
<li role="tab" class="cmp-carousel__indicator" data-cmp-hook-carousel="indicator" aria-selected="false" tabindex="-1">Rainbow</li>

        </ol>
    </div>
    
</div>
</div>
```

### JSON {#json}

```
"carousel": {
              "autoplay": false,
              "delay": 5000,
              "autopauseDisabled": false,
              ":itemsOrder": [
                "image_137106943",
                "image_162165685",
                "image"
              ],
              ":type": "weretail/components/content/carousel",
              ":items": {
                "image_137106943": {
                  "alt": "Arctic Surfing in Lofoten, Northern Norway, Europe",
                  "title": "Northern Lights",
                  "src": "/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/carousel/image_137106943.coreimg.jpeg/1543410175846.jpeg",
                  "srcUriTemplate": "/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/carousel/image_137106943.coreimg.82{.width}.jpeg/1543410175846.jpeg",
                  "areas": [],
                  "uuid": "24be0df2-92ae-4cd5-91f2-ca5a7fbf3dff",
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
                  ":type": "weretail/components/content/image",
                  "cq:panelTitle": "Northern Lights"
                },
                "image_162165685": {
                  "alt": "Arctic Surfing in Lofoten, Northern Norway, Europe",
                  "title": "Surfer Wave 02",
                  "src": "/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/carousel/image_162165685.coreimg.jpeg/1543410196033.jpeg",
                  "srcUriTemplate": "/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/carousel/image_162165685.coreimg.82{.width}.jpeg/1543410196033.jpeg",
                  "areas": [],
                  "uuid": "b55dc097-e0cb-4219-9525-dda1fb64fd8c",
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
                  ":type": "weretail/components/content/image",
                  "cq:panelTitle": "Mad-crazy waves"
                },
                "image": {
                  "alt": "Arctic Surfing in Lofoten, Northern Norway, Europe",
                  "title": "Majestic Rainbow",
                  "src": "/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/carousel/image.coreimg.jpeg/1543410210981.jpeg",
                  "srcUriTemplate": "/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten/_jcr_content/root/responsivegrid/carousel/image.coreimg.82{.width}.jpeg/1543410210981.jpeg",
                  "areas": [],
                  "uuid": "72feab95-6040-4af8-a199-a11a23e22a56",
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
                  ":type": "weretail/components/content/image",
                  "cq:panelTitle": "Rainbow"
                }
              }
            }
```

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to add, rename, and rearrange slides as well as define the auto-transition settings.

### Items Tab {#items-tab}

![](assets/screenshot_2018-10-12at102451.png)

Use the **Add** button to open the component selector to choose which component to add as a tab. Once added, an entry is added to the list, which contains the following columns:

* **Icon** - The icon of the component type of the tab for easy identification in the list. Mouse over to see the full component name as a tooltip.
* **Description** - The description used as the text of the tab, defaulting to the name of the component selected for the tab.
* **Delete** - Tap or click to delete the tab from the tabs component.
* **Reorder** - Tap or click and drag to order the tabs.

### Properties Tab {#properties-tab}

![](assets/screenshot_2018-11-28at141054.png)

On the **Properties** tab, the content author can set the slides to automatically transition.

* **Automatically transition slides** - When active, the component will automatically advance to the next slide after a specified delay.
* **Transition Delay** - When Automatically transition slides is selected, this value is used to define the delay between transitions (in milliseconds).
* **Disable automatic pause on hover** - When **Automatically transition slides** is selected, the carousel transition will automatically pause whenever the cursor hovers over the carousel. Select this option so that the transition will not pause.

>[!NOTE]
>
>The slide advance controls are not enabled when in **Edit** mode. Use [**Preview** mode](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/editing-content.html#main-pars_title_196884421) or the ** [View as Published](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/editing-content.html#main-pars_title_1534569976)** option to interact with the carousel as a reader of the published content would.
>
>The auto-advance feature is not enabled when in **Edit** mode. Use ** [View as Published](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/editing-content.html#main-pars_title_1534569976)** option to see the auto-advance feature as a reader of the published content would.

## Select Panel {#select-panel}

The content author can use the **Select Panel** option on the component toolbar to change to a different slide for editing as well as to easily rearrange the order of the slides.

![](assets/screenshot_2018-10-11at165417.png)

Once selecting the **Select Panel** option in the component toolbar, the configured slides are displayed as a drop-down.

* The list is ordered by the assigned arrangement of the slides and is reflected in the numbering.
* The component type of the slide is displayed first, followed by the description of the slide in lighter font.

![](assets/opera_snapshot_2018-11-28141537localhost.png)

* Tapping or clicking an entry in the dropdown, switches the view in the editor to that slide.
* The slide can be reordered in-place by using the drag handles.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define which components can be added as slides to the carousel component as well as define auto-transition defaults and which custom styles are available to the content author.

### Properties Tab {#properties-tab-1}

The **Properties** tab is used to define the default settings for the slide transitions when a content author adds the carousel component to a page.

![](assets/screenshot_2018-11-28at141824.png)

* **Automatically transition slides** - Defines if by default the option to automatically advance the carousel to the next slide is enabled when the content author adds the carousel component to a page.
* **Transition Delay** - Defines the default value of the transition delay between slides (in milliseconds) when a content author adds the carousel component to a page.
* **Disable automatic pause on hover** - Defines if by default the option to disable the automatic slide pausing is enabled when **Automatically transition slides** is selected by the content author.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as slides to the Carousel Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_procedure_1914319072)

### Styles Tab {#styles-tab}

The Carousel Component supports the AEM [Style System](authoring.md#component-styling).

## Technical Details {#technical-details}

The latest technical documentation about the Carousel Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel).

The entire core components project can be downloaded from GitHub.

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md). 
