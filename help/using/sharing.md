---
title: Social Media Sharing Component
seo-title: Social Media Sharing Component
description: null
seo-description: The Core Component Social Media Sharing Component is a Facebook and Pinterest sharing widget.
uuid: a75aeca9-f055-429b-a128-7d4a1e5ab21e
contentOwner: User
content-type: reference
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: a4a31261-01e9-4fda-8d1b-7cec90bb6574
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

# Social Media Sharing Component{#social-media-sharing-component}

The Core Component Social Media Sharing Component is a Facebook and Pinterest sharing widget.

## Usage {#usage}

The Sharing Component adds Facebook and Pinterest sharing links to the page. It is often included in page headers or footers.

Unlike other components, the settings for the sharing component is done by the template author via [Initial Page properties](/content/help/en/experience-manager/6-3/sites/authoring/using/templates#main-pars_title_1651978509) and by the content author via [Page Properties](/content/help/en/experience-manager/6-3/sites/authoring/using/editing-page-properties).

## Version and Compatibility {#version-and-compatibility}

The current version of the Social Media Sharing Component is v1, which was introduced with release 1.0.0 of the Core Components with AEM 6.3, and is described in this document.

The following table details all supported versions of the component and the AEM versions with which the versions of the component is compatible.

<table border="1" cellpadding="1" cellspacing="0" width="100%"> 
 <tbody> 
  <tr> 
   <td>Component Version<br /> </td> 
   <td>AEM 6.3</td> 
   <td>AEM 6.4</td> 
  </tr> 
  <tr> 
   <td>v1<br /> </td> 
   <td>Compatible</td> 
   <td>Compatible</td> 
  </tr> 
 </tbody> 
</table>

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

The following is sample taken from [We.Retail](/content/help/en/experience-manager/6-3/sites/developing/using/we-retail).

### Screenshot {#screenshot}

![](assets/chlimage_1.png) 

### HTML {#html}

```
<div class="sharing aem-GridColumn aem-GridColumn--default--12">

<div class="fb-share-button fb_iframe_widget" data-href="https://localhost:4503/content/we-retail/us/en/experience.html" data-layout="button_count" data-size="small" data-mobile-iframe="false" fb-xfbml-state="rendered" fb-iframe-plugin-query="app_id=&container_width=1152&href=http%3A%2F%2Flocalhost%3A4503%2Fcontent%2Fwe-retail%2Fus%2Fen%2Fexperience.html&layout=button_count&locale=en_US&mobile_iframe=false&sdk=joey&size=small"><span style="vertical-align: bottom; width: 69px; height: 20px;"><iframe name="fc0e02fa514178" width="1000px" height="1000px" frameborder="0" allowtransparency="true" allowfullscreen="true" scrolling="no" title="fb:share_button Facebook Social Plugin" src="https://www.facebook.com/v2.7/plugins/share_button.php?app_id=&channel=http%3A%2F%2Fstaticxx.facebook.com%2Fconnect%2Fxd_arbiter%2Fr%2FlY4eZXm_YWu.js%3Fversion%3D42%23cb%3Df1b1727c10887a8%26domain%3Dlocalhost%26origin%3Dhttp%253A%252F%252Flocalhost%253A4503%252Ff1cacf3ab0a9334%26relation%3Dparent.parent&container_width=1152&href=http%3A%2F%2Flocalhost%3A4503%2Fcontent%2Fwe-retail%2Fus%2Fen%2Fexperience.html&layout=button_count&locale=en_US&mobile_iframe=false&sdk=joey&size=small" style="border: none; visibility: visible; width: 69px; height: 20px;" class=""></iframe></span></div>
<a class="PIN_1515753862817_button_pin PIN_1515753862817_beside PIN_1515753862817_save PIN_1515753862817_padded" href="https://uk.pinterest.com/pin/create/button/?guid=40RWC84gSWNB-1&url=http%3A%2F%2Flocalhost%3A4503%2Fcontent%2Fwe-retail%2Fus%2Fen%2Fexperience.html&media=http%3A%2F%2Flocalhost%3A4503%2Fcontent%2Fwe-retail%2Fus%2Fen%2Fexperience.thumb.800.480.png%3Fck%3D1515753835&description=Experience" data-pin-log="button_pinit" data-pin-href="https://uk.pinterest.com/pin/create/button/?guid=40RWC84gSWNB-1&url=http%3A%2F%2Flocalhost%3A4503%2Fcontent%2Fwe-retail%2Fus%2Fen%2Fexperience.html&media=http%3A%2F%2Flocalhost%3A4503%2Fcontent%2Fwe-retail%2Fus%2Fen%2Fexperience.thumb.800.480.png%3Fck%3D1515753835&description=Experience" data-pin-x="0"><span class="PIN_1515753862817_count" data-pin-href="https://uk.pinterest.com/pin/create/button/?guid=40RWC84gSWNB-1&url=http%3A%2F%2Flocalhost%3A4503%2Fcontent%2Fwe-retail%2Fus%2Fen%2Fexperience.html&media=http%3A%2F%2Flocalhost%3A4503%2Fcontent%2Fwe-retail%2Fus%2Fen%2Fexperience.thumb.800.480.png%3Fck%3D1515753835&description=Experience" data-pin-log="button_pinit" data-pin-x="0">0</span>Save
</a>
</div>
```

### JSON {#json}

```
"sharing":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "facebookEnabled":true,
                     "pinterestEnabled":true,
                     "socialMediaEnabled":true,
                     "metadata":{  
                        "og:title":"Experience",
                        "og:url":"https://localhost:4503/content/we-retail/us/en/experience.json",
                        "og:type":"website",
                        "og:site_name":"We.Retail",
                        "og:image":"https://localhost:4503/content/we-retail/us/en/experience.thumb.800.480.png?ck=1515753835"
                     },
                     ":type":"weretail/components/content/sharing",
                     "hasFacebookSharing":true,
                     "hasPinteresSharing":true
                  }
```

## Edit Dialog {#edit-dialog}

Because sharing requires special page headers, any sharing must be enabled at the page level. Therefore, for the content author the edit options for the sharing component are available through the sharing tab the [page properties](/content/help/en/experience-manager/6-3/sites/authoring/using/editing-page-properties).

## Design Dialog {#design-dialog}

Because sharing requires special page headers, any sharing must be enabled at the page level. Therefore, for the template author the design options for the sharing component are available through the [initial page properties](/content/help/en/experience-manager/6-3/sites/authoring/using/templates#main-pars_title_1651978509).

## Technical Details {#technical-details}

The latest technical documentation about the Sharing Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/sharing/v1/sharing).

The entire core components project can be downloaded from GitHub.

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md). 
