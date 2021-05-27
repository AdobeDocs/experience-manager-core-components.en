---
title: AEM as a Cloud Service SDK Build Analyzer Maven Plugin
description: Documentation for the local Maven build analyzer plugin
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Administrator
exl-id: de26b310-a294-42d6-a0db-91f6036a328c
---
# AEM as a Cloud Service SDK Build Analyzer Maven Plugin {#maven-analyzer-plugin}

The AEM as a Cloud Service SDK Build Analyzer Maven Plugin analyzes the structure of the various content packages projects.

See the [Maven Plugin documentation](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) for information on how to include it in an AEM maven project. 

>[!NOTE]
>
>It is recommended that you update your Maven project to reference the latest version of the plugin found in the Maven central repository, at this location: https://repo1.maven.org/maven2/com/adobe/aem/aemanalyser-maven-plugin/

The plugin uses the latest available SDK rather than the one configured in the project.

Below is a table describing the analyzers that are executed as part of this step. <!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| Module  | Function, Example and Troubleshooting  | Local SDK  | Cloud Manager  |
|---|---|---|---|
| `api-regions-exportsimports`  |  Checks if all OSGI bundles have their Import-Package declarations satisfied by the Export-package declaration of other included bundles in the Maven project. An error would look like this: <p>&nbsp;</p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p>&nbsp;</p>To troubleshoot, see if the bundle providing the package is included in the deployment, or alternatively look at the manifest of the bundle that you would expect to be exporting to determine if the wrong name or wrong version was used.  | Yes  | Yes  |
| `requirements-capabilities`  | Checks if all the requirements declarations made in OSGI bundles are satisfied by the capabilities declarations of other bundles included in the Maven project. An error would look like this: <p>&nbsp;</p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p>&nbsp;</p> To troubleshoot, look at the manifest of the bundle that you would expect to be declaring a capability to determine why it is missing, or check in the manifest of the requiring bundle to see that the requirement in there is correct.  | Yes  | Yes  |
| `bundle-content` | Gives a warning if a bundle contains initial content specified with Sling-Initial-Content, which is problematic in the AEM as a Cloud Service clustered environment. The warning looks like this: <p>&nbsp;</p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p>&nbsp;</p>To troubleshoot convert the initial content into repoinit  statements, see Repoinit Documentation.  | Yes  | Yes  |
| `bundle-resources`  | Gives a warning if a bundle contains resources specified with the  Sling-Bundle-Resources  header, which is problematic in the AEM as a Cloud Service clustered environment. The warning looks like this:<p>&nbsp;</p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p>&nbsp;</p> To troubleshoot convert the resources to repoinit  statements, see [Repoinit Documentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=en#repo-init).  | Yes  | Yes  |
| `api-regions`<p>&nbsp;</p>`api-regions-check-order`<p>&nbsp;</p>`api-regions-dependencies`<p>&nbsp;</p>`api-regions-duplicates`  | These analyzers check some details related to the [content package to feature model conversion process](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=en#deploying) that creates artifacts conforming to the Sling Feature Model. Any errors should be reported to Adobe Customer Support.  | Yes  | Yes  |
| `api-regions-crossfeature-dups`  | Validates that customer OSGI bundles don't have Export-package declarations that override AEM as a Cloud Service's public API<p>&nbsp;</p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p>&nbsp;</p>To fix, stop exporting a package that's part of the AEM public API. | Yes  | Yes  |
| `repoinit`  | Checks the syntax of all repoinit sections | Yes  | Yes  |
| `bundle-nativecode`  | Validates that OSGI bundles do not install native code. | Yes  | Yes  |
| `configuration-api`  | Validates important OSGi configurations. | Yes  | Yes  |
|`region-deprecated-api`   | Analyser runs locally and in AEM as a Cloud Service. | Yes | Yes  |
 
