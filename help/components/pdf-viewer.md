---
title: PDF Viewer Component
description: The PDF Viewer Component allows for the display of a PDF document.
feature: Core Components
role: "Architect, Developer, Administrator, Business Practitioner"
---

# PDF Viewer Component {#pdf-viewer-component}

The Core Component PDF Viewer component allows for the inclusion of a PDF document on a page.

## Usage {#usage}

The Core Component PDF Viewer component embeds a viewer to display PDF files stored as assets on the page.

## Version and Compatibility {#version-and-compatibility}

The current version of the PDF Viewer Component is v1, which was introduced with release 2.10.0 of the Core Components in June 2020, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the PDF Viewer Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_pdfviewer).

## Technical Details {#technical-details}

The latest technical documentation about the PDF Viewer Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

>[!NOTE]
>
>The PDF Viewer Component leverages [Adobe's Document Services APIs](https://www.adobe.io/apis/documentcloud/dcsdk.html) and requires your administrator to configure a [context aware configuration](/help/developing/context-aware-configs.md) in order to use these services. Check the technical documentation of the component for [details on this configuration.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the viewer and how it will behave and appear for a visitor to the page.

### Configuration Tab {#configuration-tab}

The Configuration Tab allows the author to define which PDF should be displayed. The path can be defined as an asset in AEM or an absolute path to another resource.

![Configuration tab of the edit dialog of PDF Viewer Component](/help/assets/pdf-viewer-edit-configuration.png)

### Customize Tab {#customize-tab}

The Customize Tab allows the author to define the options available in the viewer to the reader and how the viewer should be presented.

![Customize tab of the edit dialog of PDF Viewer Component](/help/assets/pdf-viewer-edit-customize.png)

The number of options available depends on the **Type** that is selected.

* [Full Window](#full-window) - The viewing area renders in the full browser. This is best suited for storage and productivity applications.
* [Sized Container](#sized-container) - The viewing area renders in the full browser. This is best suited for storage and productivity applications.
* [In-Line](#in-line) - All PDF pages rendered in line within a web page. This is best suited for reading applications.

#### Full Window {#full-window}

The viewing area renders in the full browser. This is best suited for storage and productivity applications.

![Customize tab full window option of the edit dialog of PDF Viewer Component](/help/assets/pdf-viewer-edit-customize-full.png)

* **Default View Mode** - How the viewer will be fit to the page where it is displayed
  * Fit Page
  * Fit Width
* **Full Screen** - When enabled, the viewer will take up the full height/width of the viewport.
* **Annotation Tools** - When enabled, the annotation tools are available.
* **Left Hand Panel** - When enabled, the left hand panel is shown.
* **Download PDF** - When enabled, the download button is shown.
* **Print PDF** - When enabled, the print button is shown.
* **Page Controls** - Toggles the behavior of the page controls.
  * Dock
  * Undock

#### Sized Container {#sized-container}

The viewing area renders in the full browser. This is best suited for storage and productivity applications.

![Customize tab sized container option of the edit dialog of PDF Viewer Component](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Full Screen** - When enabled, the viewer will take up the full height/width of the viewport.
* **Download PDF** - When enabled, the download button is shown.
* **Print PDF** - When enabled, the print button is shown.
* **Page Controls** - Toggles the behavior of the page controls.
  * Dock
  * Undock

#### In-Line {#in-line}

All PDF pages rendered in line within a web page. This is best suited for reading applications.

![Customize tab sized container option of the edit dialog of PDF Viewer Component](/help/assets/pdf-viewer-edit-customize-inline.png)

* **Download PDF** - When enabled, the download button is shown.
* **Print PDF** - When enabled, the print button is shown.

## Design Dialog {#design-dialog}

There is no Design Dialog for the PDF Viewer Component.
