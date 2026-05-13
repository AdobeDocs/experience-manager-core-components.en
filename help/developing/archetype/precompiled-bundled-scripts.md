---
title: Precompiled Bundled Scripts
description: Learn how to deploy your component scripts via OSGi bundles to Adobe Experience Manager Cloud Service.
feature: Core Components, AEM Project Archetype
role: Developer, Admin
exl-id: 3edc388f-01b2-45cc-bd56-f22e5a5a8624
TQID: https://experienceleague.adobe.com/CRIKInyfl-kbar3LUOs8kHFaXO9L4kgYf8pXIopaWK0
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
---
# Precompiled Bundled Scripts {#precompiled-bundled-scripts}

AEM as a Cloud Service supports the deployment of the [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) component scripts as precompiled bundled scripts. This allows developers to precompile their scripts at build-time and package them as OSGi bundles.

## Advantages of Deploying Precompiled Scripts via OSGi Bundles {#advantages}

Deploying your scripts as precompiled bundled scripts has the following benefits:

+ Compiling scripts at build time allows developers to discover errors early in the development process.
+ Java API script dependencies are explicitly defined via the `Import-Package` and `Export-Package` bundle headers.
+ Inheritance (via `sling:resourceSuperType`) and delegation to other resource types (via HTL's `data-sly-resource` block element or via the `sling:include` JSP tag, for example) can be mapped via the bundle's meta-data.
+ Resource type versioning can be enforced in a similar way to the Java APIs.

## Precompilation and Package Imports {#precompilation}

The [`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html) can validate the syntax of HTL scripts, but it can also be used to transpile the HTL scripts into Java classes. These are then added to your Maven project's `generated-sources` folder and picked-up by the `maven-compiler-plugin`.

The [`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin) can be added to generate the OSGi bundle's metadata for Java API imports.

## Inheritance and Delegation {#inheritance-delegation}

The OSGi framework provides a powerful way of defining [requirements and capabilities](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies) to express contracts between various components. These are described via meta-data and enforced at runtime. Bundled scripts use this mechanism to express both their inheritance relationships (`sling:resourceSuperType`), as well as delegation (including other resource types in the rendering process).

The `bnd` plugin from the [scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) project can be used to extract the requirements and capabilities corresponding to the scripts provided by the [`ui.apps`.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) content package

## AEM Project Archetype Support {#support}

Starting with version 31, the [AEM Project Archetype](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html) can be used to correctly set up an AEM as a Cloud Service project to use precompiled bundled scripts.

In addition, the AEM Project Archetype configures the [AEM as a Cloud Service SDK Build Analyzer Maven Plugin](/help/developing/archetype/build-analyzer-maven-plugin.md) to validate the Java package-level as well as script-level dependencies.
