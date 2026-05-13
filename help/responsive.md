---
title: Responsive Design of the Core Components
description: Learn about the responsive design of the Core Components and how it may affect your project.
role: Developer, Admin, User
exl-id: c0eff174-6803-4b44-aeb1-eae3bc8a36ea
TQID: https://experienceleague.adobe.com/wUpRlK8WxDuQzmFJFWAwFZUY-1fo9qOOgbOn-GEwBok
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
# Responsive Design of the Core Components {#responsive-design}

All Core Components are designed to be fully responsive, ensuring a seamless experience across devices. It's important to note that some advanced components, like for example the [Carousel,](/help/components/carousel.md) [Tabs,](/help/components/tabs.md) and [Accordion Components,](/help/components/accordion.md) may require specific consideration within the context of the implementing project in order to maintain responsiveness in all conditions.

Given the diverse ways these components can exhibit responsive behavior, and in Adobe's commitment to keep the Core Components lightweight out-of-the-box, the responsibility for implementing detailed responsive aspects is intentionally left to the project.

For instance, on narrow screens the Tabs component may adapt by breaking wide tabs onto new lines, by allowing vertical scrolling, by transforming tabs into drop-downs, or by adopting an accordion style. Due to the potential impact on performance that implementing all those behaviors would cause, the [clientlibs](/help/developing/including-clientlibs.md#provided) are intended as a starting point for implementors rather than an exhaustive solution.
