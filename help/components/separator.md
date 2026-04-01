---
title: Separator Component
description: The separator component creates a break between components on a page
role: Developer, Admin, User
exl-id: 79f19368-67fa-4864-93f7-2aa801d13fdb
TQID: https://experienceleague.adobe.com/phmSUsqkY69wmGhAtWuj1qvFcjr84gPe2H90CsKVAAE
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
    internal-label: Authoring
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Separator Component {#separator-component}

The Core Component Separator Component displays a horizontal rule for separating content.

{{traditional-aem}}

## Usage {#usage}

The Separator Component allows the content author to easily create a horizontal rule as a break between content to better organize information on a page.

## Version and Compatibility {#version-and-compatibility}

The current version of the Separator Component is v1, which was introduced with release 2.3.0 of the Core Components in February 2019, and is described in this document.  
  
The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

| Component Version |AEM 6.4 |AEM 6.5 |AEM 6.5 LTS|AEM as a Cloud Service|
|---|---|---|---|---|
| v1 |Compatible with<br>[release 2.17.4](/help/versions.md) and prior|Compatible|Compatible|Compatible|

## Sample Component Output {#sample-component-output}

To experience the Separator Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_separator).

### Technical Details {#technical-details}

The latest technical documentation about the Separator Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_separator_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

![Separator Component's edit dialog](/help/assets/separator-edit.png)

* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the styles applied to the Separator Component.

### Styles Tab {#styles-tab}

The Separator Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
