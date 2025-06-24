---
title: Content Fragment List Component (v1)
description: The Core Component Content Fragment List component allows for the display of a list of content fragments.
role: Architect, Developer, Admin, User
exl-id: 37d6632d-360d-4081-8279-8efbb369a82e
index: n
---

# Content Fragment List Component (v1) {#content-fragment-list-component}

The Core Component Content Fragment List component allows for the display of a list of [content fragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html).

## Usage {#usage}

The Core Component Content Fragment List Component allows for the inclusion of a list of [content fragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) on a page based on a Content Fragment model. This can be especially useful for creating [headless content](https://helpx.adobe.com/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) that can be easily consumed by other applications.

* The list and its properties can be selected in the [configure dialog](#configure-dialog).
* Styles can be applied to the component in the [design dialog](#design-dialog).

## Version and Compatibility {#version-and-compatibility}

The document describes v1 of the Content Fragment Component, which was introduced with release 2.4.0 of the Core Components in May 2019.

>[!CAUTION]
>
>This document describes v1 of the Content Fragment List Component.
>
>For details of the current version of the Content Fragment List Component, see the [Content Fragment List Component](/help/components/content-fragment-list.md) document.

## Sample Component Output {#sample-component-output}

To experience the Content Fragment List Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_cflist).

## Technical Details {#technical-details}

The latest technical documentation about the Content Fragment List Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_cflist_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the which content fragments comprise the list and the elements of those fragments to be included.

### Properties Tab

The **Properties** tab defines which Content Fragments are included in the list. This is primarily based on a selected Content Fragment Model, but there are other filter options available.

![Properties tab of the edit dialog of the Content Fragment List Component](/help/assets/content-fragment-list-properties.png)

* **Model** - Path to the Content Fragment Model on which the list is based.
  * By default, all content fragments of the model defined as **Model Path** are included in the list.
* **Parent Path** - Parent path from which the list should be built.
  * The content fragments based on the selected **Model Path** will be filtered to those on the specified **Parent Path**.
    * Click or tap the **Open Selection Dialog** button at the right side of the field to specify the path.
* **Tags** - Only the Content Fragments with the specified tags will be included in the list.
  * Click or tap the **Open Selection Dialog** button at the right side of the field to specify the tags.
  * Click or tap the X next to selected tags to remove them.
* **Order By** - Field of the content fragment model by which the list will be ordered
  * Only text fields (including numeric, date, and time) are selectable.
* **Sort Order** - How the list will be sorted by the **Order By** field
  * Ascending or descending
* **Max Items** - Maximum number of items to be shown in the list
  * No value will return all items.
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

>[!NOTE]
>The **Order By**, **Sort Order**, and **Max Items** options were introduced with release 2.7.0 of the Core Components.

### Elements Tab

By default, all elements of the Content Fragment Model will be included in the list (unless limited by the **Max Items** field). The **Elements** tab allows you to specify only specific elements to include.

![Elements tab of the edit dialog of the Content Fragment List Component](/help/assets/content-fragment-list-elements.png)

* **Elements** - Only the elements of the content fragments in the list specified will appear.
  * Click or tap the **Add** button to add a new element.
  * Click or tap the **Delete** button to remove a selected element.
  * Drag the **Order** handle to rearrange the order of the elements.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the styles applied to the Content Fragment List Component.
