---
title: Developing Core Components
description: The Core Components provide robust and extensible base components which offer feature-rich capabilities, continuous delivery, component versioning, modern implementation, lean markup, and JSON export of content.
role: Architect, Developer, Administrator
---

# Developing Core Components {#developing-core-components}

## When to Use the Core Components? {#when-to-use-the-core-components}

As the Core Components are all-new, and offer multiple benefits, it is recommended for new AEM projects to use them. For existing projects, a migration should be part of a larger project effort, for example a rebranding or overall refactoring.

Therefore, Adobe provides following recommendations:

* **New Projects**
  New projects should always attempt to use Core Components. If Core Components cannot be used directly or [extended](customizing.md) to satisfy project requirements, then create a custom component following the component architecture set forth in core components. Except where not otherwise possible, avoid using the [foundation components](/help/versions.md#foundation-component-support).  
* **Existing Projects**
  Recommendation is keep using the [foundation components](/help/versions.md#foundation-component-support), unless a site or component refactoring is planned.  
  As they are very widely used by most existing projects, the foundation components [will continue to be supported.](/help/versions.md#foundation-component-support)
* **New Custom Components**
  Assess if an existing [Core Component may be customized](customizing.md).  
  If not, recommendation is to build a new custom component following the [Component Guidelines](guidelines.md).
* **Existing Custom Components**
  If your components work as expected, then keep them as they are.  
  If not, refer to "New Custom Components" above.

## How to Succeed with the Core Components {#how-to-succeed}

The Core Components are powerful, flexible, and easy to use and customize. [Following a few key guidelines](success.md) will ensure that your project with the Core Components is a success.

## Migrating to the Core Components

Any new project should be implemented with Core Components. However existing projects will usually have extensive implementations of the Foundation Components.

A larger effort on an existing project (for example a rebranding or overall refactoring) often offers a chance to migrate to the Core Components. To facilitate this migration, Adobe has provided a number of migration tools to encourage the adoption of the Core Components and the latest AEM technology.

[The AEM Modernization Tools](http://opensource.adobe.com/aem-modernize-tools/) allow for the easy conversion of:

* Static templates to editable templates
* Design configurations to policies
* Foundation Components to Core Components
* Classic UI to Touch-Enabled UI

For further information about the usage of these tools, [see their documentation](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>The AEM Modernize Tools are a community effort and are not supported or warrantied by Adobe.

## Core Component Support {#core-component-support}

Core Components are an integral part of AEM and supported as is, under the same terms and conditions as if they were delivered as part of the Quickstart.

Like other AEM product features, the general rule is: Components are first announced to be deprecated, and the earliest removed for the following AEM release. That gives customers at least one release cycle to move to the new version of the component, before dropping its support.

The version of each component clearly states the AEM versions that it supports. When support ceases for a version of AEM, then so does the support of the Core Components for that version of AEM.

For details about the support of component customizations, see the [Customizing Core Components](customizing.md) page.


## Technical Capabilities {#technical-capabilities}

The following table gives an overview of the differences between core components and foundation components.

For details about their authoring capabilities and options to pre-configurable them, [refer to the authoring page about them](/help/get-started/authoring.md).

| **Capability** |**Core Component** |**Foundation Component** |
|-----|---|---|
| Logic implementation |Java POJOs with [Sling Models](https://sling.apache.org/documentation/bundles/models.html) annotations |JSP code |
| Markup definition | [HTML Template Language](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) (HTL) syntax |JSP code |
| XSS sanitization |Automated by HTL |Mostly manual  |
| CSS classes naming |Standardized naming convention based on [Block Element Modifier](https://getbem.com/) (BEM) notation (as of release 2.0.0) |Custom schemes |
| Dialog definition | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) |Coral 2 + Classic UI |
| JSON output | [Sling Models Exporter with Jackson serialization](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) |Default Sling servlet |
| Versioning | [For the model and the HTL](guidelines.md) |None |
| Testing |Unit Tests + Integration Tests |Integration Tests |
| Delivery | [Via public GitHub](https://github.com/adobe/aem-core-wcm-components) |Via Quickstart |
| License | [Apache License](https://www.apache.org/licenses/LICENSE-2.0) |Adobe proprietary |
| Contribution |Via pull request |Not possible |
| Accessibility |Fully compliant with the [WCAG 2.0 AA standard](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |Only partially compliant with the [WCAG 2.0 AA standard](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |

## Component List {#component-list}

The following table lists the available Core Components, linking to their API, and indicates which foundation components they replace.

|Core Component|Description|Replaced Foundation Component(s)|
|---|---|---|
|[Page](https://adobe.com/go/aem_cmp_tech_page_v2)|Responsive page working with template editor|`/libs/foundation/components/page /libs/wcm/foundation/components/page`|
|[Breadcrumb](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2)|Page hierarchy navigation|`/libs/foundation/components/breadcrumb`|
|[Title](https://adobe.com/go/aem_cmp_tech_title_v2)|H1-H6 title|`/libs/foundation/components/title /libs/wcm/foundation/components/title`|
|[Text](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text)|Rich text|`/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text`|
|[Image](https://adobe.com/go/aem_cmp_tech_image_v2)|Smart and lazy loading of optimal rendition size|`/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image`|
|[List](https://adobe.com/go/aem_cmp_tech_list_v2)|List of pages|`/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list`|
|[Social Media Sharing](https://adobe.com/go/aem_cmp_tech_sharing_v1)|Facebook and Pinterest sharing widget|`-`|
|[Form Container](https://adobe.com/go/aem_cmp_tech_form_container_v2)|Responsive form paragraph system|`/libs/foundation/components/form/start /libs/foundation/components/form/end`|
|[Form Text](https://adobe.com/go/aem_cmp_tech_form_text_v2)|Text input field|`/libs/foundation/components/form/text /libs/foundation/components/form/password`|
|[Form Options](https://adobe.com/go/aem_cmp_tech_form_options_v2)|Multiple options input field|`/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown`|
|[Form Hidden](https://adobe.com/go/aem_cmp_tech_form_hidden_v2)|Hidden input field|`/libs/foundation/components/form/hidden`|
|[Form Button](https://adobe.com/go/aem_cmp_tech_form_button_v2)|Submit or custom button|`/libs/foundation/components/form/submit`|
|[Navigation](https://adobe.com/go/aem_cmp_tech_navigation_v1)|A site navigation component that lists the nested page hierarchy|`/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav`|
|[Language Navigation](https://adobe.com/go/aem_cmp_tech_langnav_v1)|A language and country switcher that lists the global language structure|`-`|
|[Quick Search](https://adobe.com/go/aem_cmp_tech_search_v1)|A search component that displays the results as in-place suggestions in a drop-down menu|`/libs/foundation/components/search`|
|[Teaser](https://adobe.com/go/aem_cmp_tech_teaser_v1)|Allows the content author to easily create a teaser to further content using an image, title, or rich text and linking to further content or other actions|`-`|
|[Tabs](https://adobe.com/go/aem_cmp_tech_tabs_v1)|Allows the content author to organize page content within multiple tabs|`-`|
|[Carousel](https://adobe.com/go/aem_cmp_tech_carousel_v1)|Allows the content author to organize content in a rotating carousel of slides|`/libs/foundation/components/carousel`|
|[Content Fragment](https://adobe.com/go/aem_cmp_tech_cf_v1)|Allows for the display of a content fragment|`-`|
|[Content Fragment List](https://adobe.com/go/aem_cmp_tech_cflist_v1)|Allows for the display a list of content fragments|`-`|
|[Separator](https://adobe.com/go/aem_cmp_tech_separator_v1)|Separates content on a page|`-`|
|[Accordion](https://adobe.com/go/aem_cmp_tech_accordion_v1)|Organize content panels in a collapsible accordion|`-`|
|[Container](https://adobe.com/go/aem_cmp_tech_container_v1)|Organize components within a container|`-`|
|[Button](https://adobe.com/go/aem_cmp_tech_button_v1)|Create a button on a page|`-`|
|[Download](https://adobe.com/go/aem_cmp_tech_download_v1)|Add a downloadable asset to a page|`-`|
|[Experience Fragment](https://adobe.com/go/aem_cmp_tech_xf_v1)|Add an experience fragment to a page|`/libs/cq/experience-fragments/editor/components/experiencefragment`|
|[Embed](https://adobe.com/go/aem_cmp_tech_embed_v1)|Embed an external resource within a page|-|
|[Progress Bar](https://adobe.com/go/aem_cmp_tech_progress_v1)|Provide a visual representation of progress towards a goal|-|
|[PDF Viewer](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1)|Presents a PDF document on a page|-|

### Upcoming Components {#upcoming-components}

For an overview of the upcoming Core Component road map see the [project wiki on GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Upgrade of Core Components {#upgrade-of-core-components}

One benefit of versioned components is that it allows to separate the migration to a new AEM version from the migration to new component versions. Also, if new component versions are available, it allows for the individual migration of each component to the new version.

Migrations to a new AEM version won't impact how the Core Components work, provided that their versions also support the new AEM version that is being migrated to. Customizations made to the Core Components should not be affected either, as long as they don't use APIs that have been [deprecated or removed](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html).

Migrations to new versions of the Core Components won't impact how the component works either, but new features might be introduced to page authors, which might require some configuration by a template editor, in case the default behavior isn't desired. Customizations however might need to be adapted, for more details see the [Customizing Core Components](customizing.md#upgrade-compatibility-of-customizations) page.
