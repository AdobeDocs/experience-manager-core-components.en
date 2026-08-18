---
title: Configuring Content AI Search Component
description: The Content AI Search component provides your site visitors with an generative AI-powered search. Learn how to enable this component for your content authors.
role: Developer, Admin
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
    internal-label: Authoring
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
    internal-label: Mobile experience
---

# Configuring Content AI Search Component {#configure-content-ai-search-component}

The Content AI Search component provides your site visitors with an generative AI-powered search. Learn how to enable this component for your content authors.

## Prerequisites {#prerequisites}

* At least one [Content Source](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) already created and with the status **Available**.
* The **AEM Content AI Client** OSGi configuration (`ContentAIClientImpl`) set up on both author and publish, with a valid API credential and a **Default Content Source** value. Please see the document [Set Up an Adobe Developer Console Project](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/setup-adc-project) for how to obtain credentials.

## Create a Proxy Component {#proxy-component}

Like all Core Components, it is recommended to create a proxy component for the default Content AI Search Component that ships with AEM. By keeping your project-specific changes in the proxy component under `/apps`, the base components under `/libs` is updated by Adobe automatically and your project component automatically inherits these updates. Please see the documents [Using Core Components](/help/get-started/using.md#aemaacs) and [Component Guidelines](/help/developing/guidelines.md) for more information.

## Configure Client Libraries {#clientlib}

Once the proxy component is created, you can enable client libraries for it. Please see the document [Client Libraries and the Core Components](/help/developing/including-clientlibs.md) for more information.

## Using the Content AI Search Component {#using}

Your content authors can now place the Content AI Search Component on their pages. Please see the document [Content AI Search Component](/help/components/ai-search.md) for more information.

## How the Component Uses Content AI {#how-it-works}

* Standard search queries are served by the same retrieval layer as the Content Source's index, returning matching pages, fragments, or assets from the configured source.
* When the AI-generated summary is enabled, the component additionally calls the AEM Content AI generative endpoint, grounding the response in the same indexed content, and displays sources alongside the summary so visitors can verify it.
* Because both features read from the same governed Content Source, results and summaries stay consistent with whatever content is currently indexed. Re-running acquisition (see [Control your Content Sources](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources)) refreshes both.

## Next Steps {#next-steps}

* [Control your Content Sources](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) — Create and manage the Content Source this component searches.
* [Set Up an Adobe Developer Console Project](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/setup-adc-project) — Obtain the credentials used by the OSGi Content AI Client configuration.
* [Content AI API reference](https://developer.adobe.com/experience-cloud/experience-manager-apis/api/experimental/contentai/) — Understand the underlying search and generative-summary endpoints this component calls.
