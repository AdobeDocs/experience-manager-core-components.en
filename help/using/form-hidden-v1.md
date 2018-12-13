---
title: Form Hidden Component (v1)
seo-title: Form Hidden Component (v1)
description: null
seo-description: The Core Component Form Hidden component allows for the display of a hidden field.
uuid: f5005346-def5-4e1f-8f93-e4cfc67a9329
content-type: reference
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: d35f4e71-ec7f-4128-9123-b997dbb5f0cf
disttype: dist5
gnavtheme: light
groupsectionnavitems: no
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
noindex: true
index: y
internal: n
snippet: y
---

# Form Hidden Component (v1){#form-hidden-component-v}

The Core Component Form Hidden component allows for the display of a hidden field.

## Usage {#usage}

The Core Component Form Hidden Component allows for the creation of hidden fields to pass information about the current page back to AEM and is intended to be used along with the [form container component](../using/form-container.md).

The field properties can be defined by the content editor in the [configure dialog](../using/form-hidden-v1.md#main-pars_title).

## Version and Compatibility {#version-and-compatibility}

This document describes v1 of the Form Hidden Component, originally introduced with release 1.0.0 of the Core Components with AEM 6.3.

The following table lists the compatibility of v1 of the Form Hidden Component.

<table border="1" cellpadding="1" cellspacing="0" width="100%"> 
 <tbody> 
  <tr> 
   <td><strong>AEM Version</strong></td> 
   <td><strong>Form Hidden <br /> Component v1</strong><br /> </td> 
  </tr> 
  <tr> 
   <td>6.3</td> 
   <td>Compatible</td> 
  </tr> 
  <tr> 
   <td>6.4</td> 
   <td>Compatible</td> 
  </tr> 
 </tbody> 
</table>

>[!CAUTION]
>
>This document describes v1 of the Form Hidden Component.
>
>For details of the current version of the Form Hidden Component, see the [Form Hidden Component](../using/form-hidden.md) document.

## Sample Component Output {#sample-component-output}

The following is sample taken from [We.Retail](/content/help/en/experience-manager/6-3/sites/developing/using/we-retail).

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
  <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
   <div class="visible aem-GridColumn aem-GridColumn--default--12">
    <input type="hidden" id="ghostToast" name="Invisible Toast" value="ghostToast">
   </div>
 </form>
</div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "hidden": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/hidden",
                  "name": "Invisible Toast",
                  "id": "ghostToast",
                  "value": "ghostToast"
                }
              },
              ":itemsOrder": [
                "hidden"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>JSON export from the Core Components requires release 1.1.0 of the Core Components. Please see the [compatibility information for Core Components v1](../using/versions.md#main-pars_title_236368006) for more information.

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the parameters of the hidden field.

![](assets/chlimage_1.png)

* **Name** - The name of the field, which is submitted with the form data
* **Value** - The value of the field, which is submitted with the form data
* **Identifier** - The identifier should be unique on the page and can be used to bind scripts to this form field

## Design Dialog {#design-dialog}

There is no design dialog for the Form Hidden component.

## Technical Details {#technical-details}

The latest technical documentation about the Form Hidden Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

The entire core components project can be downloaded from GitHub.

Further details about developing Core Components can be found in the [Core Components developer documentation](../using/developing.md). 
