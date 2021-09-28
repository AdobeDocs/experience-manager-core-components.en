---
title: Precompiled Bundled Scripts
description: Learn how to deploy your component scripts via OSGi bundles to Adobe Experience Manager Cloud Service.
exl-id: 3edc388f-01b2-45cc-bd56-f22e5a5a8624
---
# Precompiled Bundled Scripts

AEM as a Cloud Service supports the deployment of the [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) component scripts as precompiled bundled scripts. This allows developers to precompile their scripts at build-time and package them as OSGi bundles.

## The advantages of deploying precompiled scripts via OSGi bundles

Deploying your scripts as precompiled bundled scripts has the following benefits:

+ compiling scripts at build time allows developers to discover errors early in the development process
+ Java API script dependencies are explicitly defined via the `Import-Package` and `Export-Package` bundle headers
+ inheritance (via `sling:resourceSuperType`) and delegation to other resource types (via HTL's `data-sly-resource` block element or via the `sling:include` JSP tag, for example) can be mapped via the bundle's meta-data
+ resource type versioning can be enforced in a similar way to the Java APIs

## Precompilation and package imports

The [`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html) can validate the syntax of HTL scripts, but it can also be used to transpile the HTL scripts into Java classes. These are then added to your Maven project's `generated-sources` folder and picked-up by the `maven-compiler-plugin`.

The [`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin) can be added to generate the OSGi bundle's metadata for Java API imports.

## Inheritance and delegation

The OSGi framework provides a powerful way of defining [Requirements and Capabilities](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies) to express contracts between various components. These are described via meta-data and enforced at runtime. Bundled scripts use this mechanism to express both their inheritance relationships (`sling:resourceSuperType`), as well as delegation (including other resource types in the rendering process).

The `bnd` plugin from the [scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) project can be used to extract the Requirements and Capabilities corresponding to the scripts provided by the [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) content package.

## AEM Project Archetype support

Starting with version 31, the [AEM Project Archetype](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html) can be used to correctly set up an AEM as a Cloud Service project to use precompiled bundled scripts. In addition, the AEM Project Archetype configures the [AEM as a Cloud Service SDK Build Analyzer Maven Plugin](/help/developing/archetype/build-analyzer-maven-plugin.md) to validate the Java package-level as well as script-level dependencies.
