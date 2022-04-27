---
title: AEM as a Cloud Service SDK Build Analyzer Maven Plugin
description: Documentation for the local Maven build analyzer plugin
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
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
| `configuration-api`  | Validates important OSGi configurations. <p>&nbsp;</p> `Configuration org.apache.felix.webconsole.internal.servlet.OsgiManager: Configuration is not allowed (com.mysite:mysite.all:1.0.0-SNAPSHOT\|com.mysite:mysite.ui.config:1.0.0-SNAPSHOT)` | Yes  | Yes  |
|`region-deprecated-api`   | Checks if [deprecated api](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-apis.html) is used <p>&nbsp;</p>`[WARNING] com.mysite:mysite.core:1.0.0-SNAPSHOT: Usage of deprecated package found : org.apache.sling.settings : Avoid these features at runtime: run modes, file system access (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | Yes | Yes  |
| `artifact-rules`    | Validates dependencies like bundles and content packages to prevent known issues in artifacts.<p>&nbsp;</p>`[WARNING] [artifact-rules] com.adobe.acs:acs-aem-commons-bundle:5.0.4: Use at least version 5.0.10 (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | Yes | Yes  |
| `content-package-validation`    | Executes filevault validators. By default jackrabbit-docviewparser is enabled which checks for well-formed content syntax of xml inside packages that will be installed during deployment.<p>&nbsp;</p>`[main] WARN org.apache.sling.feature.analyser.task.impl.CheckContentPackages - ValidationViolation: "jackrabbit-docviewparser: Invalid XML found: The reference to entity "se" must end with the ';' delimiter.", filePath=jcr_root/apps/somename/configs/com.adobe.test.Invalid.xml, nodePath=/apps/somename/configs/com.adobe.test.Invalid`<p>&nbsp;</p>To fix, check the file named by the analyzer for xml issues. | Yes | Yes  |
 
## Known Issues

Below is a list of known issues when using the Build Analyzer Maven Plugin.

### Failed to Execute Build Analyzer Maven Plugin in Local SDK

When using the local SDK with a Build Analyzer Maven Plugin version lower than `1.1.2`, running the plugin might result in the below error. In this case update your project to the latest version of the plugin.

```txt
[ERROR] Failed to execute goal com.adobe.aem:aemanalyser-maven-plugin:1.1.0:analyse (default-analyse) on project mysite.analyse: Execution default-analyse of goal com.adobe.aem:aemanalyser-maven-plugin:1.1.0:analyse failed: arraycopy: source index -1 out of bounds for char[65536] -> [Help 1]
```

If you used the AEM Project Archetype to setup your project, make sure to adjust the property in the root Maven `pom.xml` like below.

```xml
   ...
   <properties>
      ...
      <aemanalyser.version>1.1.2</aemanalyser.version> <!-- Make sure to use the latest release -->
      ...
   </properties>
```
