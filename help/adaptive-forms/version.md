---
title: AEM Adaptive Forms Core Components Versions
description: AEM Core Components are published as releases which may contain more than one version of the same core components. This document explains what releases and versions are and how to understand compatibility with Core Components and AEM.
role: Architect, Developer, Admin, User
exl-id: 8146a5b1-acf6-4b54-ad6b-6e1747a137f6
---

# Adaptive Forms Core Components releases {#core-components-versions}

Identify the precise versions of both Forms Core Components and WCM Core Components dependencies. Additionally, familiarize yourself with the components and features enabled in each release of Adaptive Forms Core Components.

## AEM Forms as Cloud Service version history {#aem-as-cs-version-history}

The Core Components releases that are compatible with AEM as a Cloud Service are available on [GitHub along with comprehensive details of their releases](https://github.com/adobe/aem-core-forms-components/releases).

To see the Core Components version history for AEM as a Cloud Service, [click here](https://github.com/adobe/aem-core-forms-components/blob/master/VERSIONS.md). 


<!--
| Forms Core Components | WCM Core Components | AEM Forms as a cloud service | Java  | Maven  |  
|-----------------------|---------------------| ---------------------------- | ----- | ------ |
| 3.0.8                | 2.24.2             | Continual                    | 8, 11 | 3.3.9+ |
| 3.0.6                | 2.24.2             | Continual                    | 8, 11 | 3.3.9+ |
| 3.0.4                 | 2.24.2             | Continual                    | 8, 11 | 3.3.9+ |
| 3.0.2                 | 2.24.2             | Continual                    | 8, 11 | 3.3.9+ |
| 3.0.0                 | 2.24.2             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.90                | 2.23.4             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.88                | 2.23.4             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.86                | 2.23.4             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.76                | 2.23.4             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.74                | 2.23.4             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.72                | 2.23.4             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.70                | 2.23.4             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.68                | 2.23.2             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.66                | 2.23.2             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.64                | 2.23.2             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.62                | 2.23.2             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.60                | 2.23.0             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.56                | 2.23.0             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.54                | 2.23.0             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.52                | 2.23.0             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.50                | 2.23.0             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.48                | 2.23.0             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.46                | 2.23.0             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.44                | 2.23.0              | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.42                | 2.23.0              | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.40                | 2.23.0              | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.36                | 2.23.0              | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.26                | 2.22.12             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.18                | 2.22.10             | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.14                | 2.21.2              | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.6                 | 2.21.2              | Continual                    | 8, 11 | 3.3.9+ |                      |                     |                              |       |        |
| 2.0.4                 | 2.21.2              | Continual                    | 8, 11 | 3.3.9+ |
| 2.0.2                 | 2.21.2              | Continual                    | 8, 11 | 3.3.9+ |
| 1.1.8                 | 2.21.2              | Continual                    | 8, 11 | 3.3.9+ |
| 1.1.6                 | 2.21.2              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.56                | 2.21.2              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.54                | 2.21.0              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.52                | 2.21.0              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.50                | 2.21.0              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.48                | 2.21.0              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.46                | 2.21.0              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.44                | 2.21.0              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.42                | 2.20.8              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.40                | 2.20.8              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.38                | 2.20.8              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.36                | 2.20.8              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.34                | 2.20.8              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.30                | 2.20.8              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.28                | 2.20.8              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.26                | 2.20.8              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.24                | 2.20.2              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.22                | 2.20.2              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.20                | 2.20.2              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.18                | 2.20.2              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.16                | 2.19.0              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.14                | 2.19.0              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.12                | 2.19.0              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.10                | 2.19.0              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.8                 | 2.18.0              | Continual                    | 8, 11 | 3.3.9+ |
| 1.0.4                 | 2.18.0              | Continual                    | 8, 11 | 3.3.9+ |  
| 1.0.2                 | 2.10.0              | Continual                    | 8, 11 | 3.3.9+ |  


|Release|Description|AEM as a Cloud Service|Java&trade;|Release Date|
|---|---|---|---|---|
|[2.0.76](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.76)| With this release, the style tab and custom properties tab are fixed for Terms and Conditions component. This release also fixed Radio button component to save boolean value for the first click.|Continual|8, 11|15 November 2023|
|[2.0.74](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.74)| With this release, submission error is updated for Submit action in AEM Forms.|Continual|8, 11|15 November 2023|
|[2.0.70](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.70)| This release added support to handle sites page language in form container.|Continual|8, 11|10 November 2023|
|[2.0.64](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.64)| Support rich text for labels for Radio/checkbox  components. With this release, support for the Switch component is also added. This release also includes fixes for Terms and Condition component.|Continual|8, 11|6 November 2023|
|[2.0.62](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.62)|With this release, support for Terms and Conditions component is added. Also added support for Qualified name in core components. |Continual|8, 11|16 October 2023|
|[2.0.60](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.60)|This release includes fixes related to custom properties feature, Wizard, and Date Picker component.|Continual|8, 11|12 September 2023|
|[2.0.56](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.56)| With this release support for custom properties for all the core components are added.|Continual|8, 11|12 September 2023|
|[2.0.54](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.54)| This release fixed the issue related to localization with Date Picker component.|Continual|8, 11|30 August 2023|
|[2.0.52](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.52)| Support for using checkbox component in an Adaptive Form.|Continual|8, 11|25 August 2023|
|[2.0.50](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.50)| Added support for form fragments in an Adaptive Form with this release.|Continual|8, 11|4 August 2023|
|[2.0.48](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.48)| The major improvements in this release are related to Lighthouse performance.|Continual|8, 11|25 July 2023|
|[2.0.42](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.42)| The release incorporates improvements at programming end.|Continual|8, 11|18 July 2023|
|[2.0.38](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.38)| The accessibility feature is improved with this release.|Continual|8, 11|17 July 2023|
|[2.0.36](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.36)| With this release, you can use the custom error handler using the Rule Editor's Invoke Service.|Continual|8, 11|3 July 2023|
|[2.0.34](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.34)| Added localization support for default error messages along with Add/Remove button for Repeatable component.|Continual|8, 11|28 June 2023|
|[2.0.32](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.32)|With this release support for Captcha is added for Adaptive Forms.|Continual|8, 11|15 June 2023|
|[2.0.26](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.26)|Support for adding Adaptive forms on AEM Sites.|Continual|8, 11|7 June 2023|
|[2.0.18](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.18)|With this release, support for a repeatability for Accordion component. Also added a new component as vertical tabs.|Continual|8, 11|5 June 2023|
|[2.0.10](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.10)|With this release, support for an Adaptive Form Container component is introduced in the editor of Sites.|Continual|8, 11|17 March 2023|
|[2.0.8](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.8)|Repeatability feature for the wizard component is introduced in this release.|Continual|8, 11|03 March 2023|
|[2.0.6](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.6)|Multiple formats for the numeric input core component are introduced in this release.|Continual|8, 11|08 February 2023|
|[2.0.4](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.6)|Core component support for AEM as a Cloud Service is introduced in this release.|Continual|8, 11|30 January 2023|

--> 

## AEM 6.5 Forms version history {#aem-as-form-version-history}

The Core Components releases that are compatible with AEM 6.5 Form on premise and AMS which are available on [GitHub along with comprehensive details of their releases](https://github.com/adobe/aem-core-forms-components/releases).

To see the Core Components version history for AEM 6.5 Form on premise and AMS, [click here](https://github.com/adobe/aem-core-forms-components/blob/release/650/VERSIONS.md).

<!--
| Forms Core Components | WCM Core Components | AEM 6.5 | Java  | Maven  |  
|-----------------------|---------------------|---------| ----- | ------ |
| 1.1.34                | 2.24.2              | 6.5.18+ | 8, 11 | 3.3.9+ |
| 1.1.32                | 2.23.2              | 6.5.18+ | 8, 11 | 3.3.9+ |
| 1.1.28                | 2.23.2              | 6.5.19+ | 8, 11 | 3.3.9+ |
| 1.1.26                | 2.23.2              | 6.5.17+ | 8, 11 | 3.3.9+ |
| 1.1.24                | 2.22.12             | 6.5.17+ | 8, 11 | 3.3.9+ |
| 1.1.22                | 2.22.12             | 6.5.17+ | 8, 11 | 3.3.9+ |
| 1.1.20                | 2.22.10             | 6.5.17+ | 8, 11 | 3.3.9+ |
| 1.1.18                | 2.21.2              | 6.5.17+ | 8, 11 | 3.3.9+ |
| 1.1.16                | 2.21.2              | 6.5.17+ | 8, 11 | 3.3.9+ |
| 1.1.12                | 2.21.2              | 6.5.16+ | 8, 11 | 3.3.9+ |
 
|Release|Description|WCM Version|AEM 6.5|Java&trade;|Release Date|
|---|---|---|---|---|---|
|[1.1.32](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.32)|This release updated the information for package information of AEM Service Pack 6.5.18.0.| - |6.5.16.0+ |8, 11|15 October 2023|
|[1.1.28](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.28)|Support rich text for labels for Radio/checkbox  components. This release also includes support for Terms and Condition component and Switch components.| - |6.5.16.0+ |8, 11|15 October 2023|
|[1.1.26](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.26)|With this release added support for checkbox component for Adaptive Form and form fragments. It also includes improvements in  Lighthouse performance. The custom error handler using Rule Editor's Invoke Service is also included in this release.| - |6.5.16.0+ |8, 11|15 October 2023|
|[1.1.24](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.24)|Added localization support for default error messages along with Add/Remove button for Repeatable component. Also added support for recaptcha in Adaptive Forms.| - |6.5.16.0+ |8, 11|29 June 2023|
|[1.1.22](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.22)|Support for adding Adaptive forms on AEM Sites. Added Items tab in edit dialog of Wizard and Vertical Tabs component.| - |6.5.16.0+ |8, 11|07 June 2023|
|[1.1.16](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.16)|| - |6.5.17.0+ |8, 11|07 June 2023|
|[1.1.12](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.12)|Core component support for AEM Forms on premise and AMS, is introduced in this release.| 2.21.2 |6.5.16.0+ |8, 11|08 February 2023|
-->



## See Also {#see-also}

{{see-also}}
