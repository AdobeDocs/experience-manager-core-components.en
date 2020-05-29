---
title: Progress Bar Component
description: The progress bar component visually represents progress towards a goal
---

# Progress Bar Component {#progress-bar-component}

The Core Component Progress Bar Component visually represents progress towards a goal.

## Usage {#usage}

The Progress Bar Component allows the content author to easily create a progress bar by defining a percentage of completion, allowing for intuitive visual display of progress towards a goal.

## Version and Compatibility {#version-and-compatibility}

The current version of the Progress Bar Component is v1, which was introduced with release 2.9.0 of the Core Components in May 2020, and is described in this document.  
  
The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

| Component Version |AEM 6.4 |AEM 6.5 |AEM as a Cloud Service|
|---|---|---|---|
| v1 |Compatible |Compatible|Compatible|

## Sample Component Output {#sample-component-output}

To experience the Progress Bar Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_progress).

### Technical Details {#technical-details}

The latest technical documentation about the Progress Bar Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_progress_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

![Progress Bar Component's edit dialog](/help/assets/progress-bar-edit.png)

* **Completion** - The progress as represented by a percentage
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the styles applied to the Progress Bar Component.

### Styles Tab {#styles-tab}

The Progress Bar Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
