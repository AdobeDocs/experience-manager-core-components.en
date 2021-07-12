---
title: Paths to Success with the Core Components
description: How to succeed when implementing your project with the Core Components
role: Architect, Developer, Admin, User
exl-id: 1ea8cd1c-8435-4ded-82dc-5a7896c53e0c
---
# Paths to Success with the Core Components {#paths-to-success}

The Core Components are powerful, flexible, and easy to use and customize. Following a few key guidelines as outlined in this document will ensure that your project with the Core Components is a success.

## Two Paths to Success {#two-paths}

There are two basic approaches to implementing the core components, which can lead to success but have their own trade-offs that need to be considered on a project-by-project basis.

1. Map your designs to the Core Components and take the HTML that they provide. Or
1. If you have to comply with already-defined HTML standards you will need more effort and not get all of the benefits of the core components.

## Common Pitfalls in Component Implementation {#common-pitfalls}

Two common issues that lead to projects not succeeding with Core Components are:

* **Finalized designs** - These might even be C-level approved and are handed over to the development team to be implemented pixel-perfect without concern for the underlying technology.
* **A company-wide HTML style-guide** - Such guides too often  must be followed dogmatically by the components applying styles from a top-down perspective.

In both cases, the requirements made to the components are so tight and specific, that it’s hard to make the Core Components or any out-of-the-box component comply with them, leading to the massive development of custom components.

## Start Early {#start-early}

Instead of only considering the Core Components at the implementation phase of your project, already start with the Core Components during the wireframing and design phase.

### Use the Component Library {#component-library}

Reference the [Component Library](https://adobe.com/go/aem_cmp_library) already in the design phase. The Core Components are powerful and flexible and can take you far as a starting point. Only add custom components when there’s a real business need that truly cannot be reasonably achieved with a Core Component.

### Use the UI Kit for Adobe XD {#ui-kit}

As soon as there is a proven need for a custom component, leverage the [UI kit for Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd)  so that the designers can start building the wireframes and the designs with the Core Components as building blocks.

## Don't Overlook Powerful Features {#powerful-features}

Features of AEM and the Core Components can be very powerful, but also very subtle and the possibilities for certain functionality might not be immediately apparent to a designer.

### Content Fragments {#content-fragments}

[Content Fragments](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html) allow you to create channel-neutral content, together with (possibly channel-specific) variations. You can then use these fragments, and their variations, when authoring your content pages.

Together with the updated JSON exporter, structured content fragments can also be used to deliver AEM content via Content Services to channels other than AEM pages.

### Experience Fragment Templates {#experience-fragment-templates}

If an author wants to re-use parts (a fragment of an experience) of a page. Without [Experience Fragments,](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html) the author would need to copy and paste that fragment. Creating and maintaining these copy/paste experiences is time-consuming and prone to user errors. Experience Fragments eliminate the need for copy/paste.

### The Embed Component {#embed-component}

[The Embed Component](/help/components/embed.md) not only allows for simple inclusion of external resources such as YouTube video content, but is also extensible to allow it to accommodate content specific to a project's needs.
