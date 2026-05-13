---
title: Title Component (v1)
description: The Core Component Title Component is a section heading component that features in-place editing.
index: false
role: Developer, Admin, User
exl-id: 79549ac0-82f2-4ea0-9cce-d534d0b47b5c
TQID: https://experienceleague.adobe.com/pctqDaQdDE13Md5ubCounfF-7u7r7dha-wzLB20kLjQ
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Title Component (v1) {#title-component-v}

The Core Component Title Component is a section heading component that features in-place editing.

## Usage {#usage}

The Title Component is intended to be used as the title or heading of a section of content.

The available heading levels can be defined by the template author in the [design dialog](#design-dialog). The content editor can select from available headings levels in the [edit dialog](#edit-dialog). For added convenience, simple in-place editing of the heading text is also available.

## Version and Compatibility {#version-and-compatibility}

This document describes v1 of the Title Component, originally introduced with release 1.0.0 of the Core Components with AEM 6.3.

The following table lists the compatibility of v1 of the Title Component.

|AEM Version|Title Component v1|
|--- |--- |
|6.3|Compatible|
|6.4|Compatible|

>[!CAUTION]
>
>This document describes version 1 of the Title Component.
>
>For details of the current version of the Title Component, see the [Title Component](/help/components/title.md) document.

## Sample Component Output {#sample-component-output}

The following is sample taken from [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](/help/assets/chlimage_1-36.png) 

### HTML {#html}

```
<div class="cmp cmp-title aem-GridColumn aem-GridColumn--default--12">
     <h2>Welcome! This is our finest equipment!</h2>
</div>
```

### JSON {#json}

```
"title": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/title",
              "jcr:title": "Welcome! This is our finest equipment!",
              "type": "h2"
            }
```

>[!NOTE]
>
>JSON export from the Core Components requires release 1.1.0 of the Core Components. Please see the [compatibility information for Core Components v1](/help/versions.md) for more information.

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to define the title text as well as select the heading level.

>[!NOTE]
>
>An empty value for the title will cause the page title to be displayed.

![](/help/assets/chlimage_1-91.png)

The in-place editor can also be used to edit the text of the title component.

![](/help/assets/chlimage_1-37.png) 

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the default heading level that title components will have when created by the content authors.

![](/help/assets/chlimage_1-92.png) 

## Technical Details {#technical-details}

The latest technical documentation about the Title Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title).

The entire core components project can be downloaded from GitHub.

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).
