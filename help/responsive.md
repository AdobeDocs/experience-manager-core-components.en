---
title: Responsive Design of the Core Components
description: Learn about the responsive design of the Core Components and how it may affect your project. 
role: Architect, Developer, Admin, User
---

# Responsive Design of the Core Components {#responsive-design}

All Core Components are designed to be fully responsive, ensuring a seamless experience across devices. It's important to note that some advanced components, like for example the [Carousel,](/help/components/carousel.md) [Tabs,](/help/components/tabs.md) and [Accordion Components,](/help/components/accordion.md) may require specific consideration within the context of the implementing project in order to maintain responsiveness in all conditions.

Given the diverse ways these components can exhibit responsive behavior, and in Adobe's commitment to keep the Core Components lightweight out-of-the-box, the responsibility for implementing detailed responsive aspects is intentionally left to the project.

For instance, on narrow screens the Tabs component may adapt by breaking wide tabs onto new lines, by allowing vertical scrolling, by transforming tabs into drop-downs, or by adopting an accordion style. Due to the potential impact on performance that implementing all those behaviors would cause, the [clientlibs](/help/developing/including-clientlibs.md#provided) are intended as a starting point for implementors rather than an exhaustive solution.
