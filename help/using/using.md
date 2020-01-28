---
title: Using Core Components
description: "To get up-and-running with Core Components in your own project, there are three steps to follow: download and install, create proxy components, load the core styles, and allow the components on your templates."
---

# Using Core Components{#using-core-components}

To get up-and-running with [Core Components](developing.md) in your own project, there are four steps, which are individually detailed in sections below:

1. [Download and Install](#download-and-install)
1. [Create Proxy Components](#create-proxy-components)
1. [Load the Core Styles](#load-the-core-styles)
1. [Enable the Components](#allow-the-components)

>[!NOTE]
>
>Alternatively, for broader instructions on how to get started from scratch with the project setup, the Core Components, Editable Templates, Client Libraries and component development, the following multi-part tutorial might be of interest:  
>[Getting Started with AEM Sites - WKND Tutorial](wknd-tutorial.md)

## Download and Install {#download-and-install}

One of the driving ideas behind the core components is flexibility. Releasing new versions of the Core Components more often allows Adobe to be more flexible in delivering new features. Developers in turn can be flexible in which components they choose to integrate into their projects and how often they wish to update them.

For this reason, the Core Components are not part of the quickstart when starting in production mode (without sample content). Therefore, your first step is to [download the latest released content package from GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) and to install it on your AEM environments.

There are several ways to automate this, but the simplest way to quickly install a content package on an instance is by using the Package Manager; see [Install Packages](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#installing-packages). Also, once you'll have a publish instance running as well, you'll need to replicate that package to the publisher; see [Replicating Packages](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#replicating-packages).

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:42:59.142-0400

Should we be promoting embedding the core-component package as an artifact in a customer application, reasoning as follows: 1) a customer application is required to leverage core components (at a minimum, proxy components must be defined) 2) a customer application must be updated to leverage new versions of core components (since it requires adjusting the sling:resourceSuperType to point at the new version of the component) It seems the only time theres an advantage to installing a release directly is if a bug-fix (non version-changing) release of core-components is cut, and it doesnt coincide with an application deployment. WDYT? For example, recommend doing this for ACS Commons which has a similar use-case (https://adobe-consulting-services.github.io/acs-aem-commons/pages/maven.html) We can of course keep the instructions for manually deploying, since some will want to do this, or the bug-fix use-case will appear.

 -->

## Create Proxy Components {#create-proxy-components}

For reasons explained in the [Proxy Component Pattern](guidelines.md#proxy-component-pattern) section, Core Components must not be directly referenced from the content. To avoid that, they all belong to a hidden component group ( `.core-wcm` or `.core-wcm-form`), which will prevent them from showing up directly in the editor.

Instead, site-specific components must be created, which define the desired component name and group to display to page authors, and refer each to a Core Component as their super-type. These site-specific components are sometimes called "proxy components", because they don't need to contain anything and serve mostly to define the version of a component to use for the site. However, when customizing the [Core Components](customizing.md), these proxy components play an essential role for markup and logic customization.

So for each Core Component that is desired to be used for a site, you must:

1. Create a corresponding proxy component in the site's components folder.

   **Example**
   Under `/apps/my-site/components` create a title node of type `cq:Component`

1. Point to the corresponding Core Component version with the super-type.

   **Example**
   Add following property:  
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. Define the component's group, title, and optionally description. These values are project specific and dictate how the component is exposed to authors.

   **Example**
   Add following properties:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

For instance, look at the [title component of the We.Retail reference site](https://github.com/Adobe-Marketing-Cloud/aem-sample-we-retail/blob/master/ui.apps/src/main/content/jcr_root/apps/weretail/components/content/title/.content.xml), which is a good example of a proxy component that is built that way.

## Load the Core Styles {#load-the-core-styles}

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:57:16.414-0400

Styles is odd in that most Core Components do not have CSS; very few even have structural CSS (breadcrumbs, list) It may be more apt to title this section: Load the Core JavaScript and CSS or Load the Core Client Libraries ?

 -->

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:41:37.115-0400

This section seems to cover the "sites" clientlibs for core components; Do we need a section for ensuring the editor clientlibs are loaded in the Page Editor? Pending: https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/issues/15

 -->

<!-- 

Comment Type: annotation
Last Modified By: cotescu
Last Modified Date: 2018-03-09T10:45:52.812-0500

Load the Core Client Libraries sounds way better

 -->

1. If not done yet, create a [Client Library](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/clientlibs.html) that contains all of the CSS and JS files that are needed for your site.
1. On the Client Library of your site, add the dependencies to the Core Components that might be needed. This is done by adding an `embed` property.

   For example, to include the Client Libraries of all v1 Core Components, the property to add would be:

   ```shell
   embed="[  
   core.wcm.components.image.v1,  
   core.wcm.components.list.v1,  
   core.wcm.components.breadcrumb.v1,  
   core.wcm.components.form.container.v1,  
   core.wcm.components.form.text.v1  
   ]"
   ```

Make sure that your proxy components and client libraries have been deployed to your AEM environment before moving to the next section.

## Allow the Components {#allow-the-components}

The following steps are performed in the [Template Editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

1. In the Template Editor, select the Layout Container, and open its policy.
1. In the list of Allowed Components, select the proxy components created previously, which should show up under the component group assigned to them. Once done, apply the changes.
1. Optionally, for the components that have a design dialog, they can be pre-configured.

That's it! In the pages created from the edited template, you should now be able to use the newly created components.

**Read next:**

* [Customizing Core Components](customizing.md) - to learn how to style and customize the core components.
* [Component Guidelines](guidelines.md) - to learn the implementation patterns of the Core Components.
