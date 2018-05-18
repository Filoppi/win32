---
title: Security Channel Settings
description: Security channel settings control the way security is applied and verified on a channel.
ms.assetid: 'ad964874-0bc7-4f03-8ceb-33627ff99f08'
keywords: ["Security Channel Settings Web Services for Windows", "WWSAPI", "WWS"]
---

# Security Channel Settings

Security channel settings control the way security is applied and verified on a channel. Each security channel setting is represented by a collection of property-value pairs, with the property keys defined by the enumeration [**WS\_SECURITY\_PROPERTY\_ID**](ws-security-property-id.md). Each property in the collection has a reasonable default value. Because of these default values, it is possible to define and use a security description without specifying any of the security channel settings.

## 

[Security binding settings](security-binding-settings.md) contain similar collections of property-value pairs whose keys are defined by the [**WS\_SECURITY\_BINDING\_PROPERTY**](ws-security-binding-property.md) structure. The difference between these two sorts of settings is that the security channel settings are scoped to a security description (that is, they contain channel-wide security properties), whereas security binding settings are scoped to one of the security bindings, and there may be many security bindings. Consequently, for example, a custom security description that contains three security bindings will have one security channel settings bag for the entire channel and three security binding settings bags, one for each security binding.

The following enumerations are used with security channel settings:

-   [**WS\_PROTECTION\_LEVEL**](ws-protection-level.md)
-   [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_ID**](ws-request-security-token-property-id.md)
-   [**WS\_SECURITY\_ALGORITHM\_ID**](ws-security-algorithm-id.md)
-   [**WS\_SECURITY\_ALGORITHM\_PROPERTY\_ID**](ws-security-algorithm-property-id.md)
-   [**WS\_SECURITY\_HEADER\_LAYOUT**](ws-security-header-layout.md)
-   [**WS\_SECURITY\_HEADER\_VERSION**](ws-security-header-version.md)
-   [**WS\_SECURITY\_PROPERTY\_ID**](ws-security-property-id.md)
-   [**WS\_SECURITY\_TIMESTAMP\_USAGE**](ws-security-timestamp-usage.md)
-   [**WS\_XML\_SECURITY\_TOKEN\_PROPERTY\_ID**](ws-xml-security-token-property-id.md)

The following structures are used with security channel settings:

-   [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY**](ws-request-security-token-property.md)
-   [**WS\_SECURITY\_ALGORITHM\_PROPERTY**](ws-security-algorithm-property.md)
-   [**WS\_SECURITY\_ALGORITHM\_SUITE**](ws-security-algorithm-suite.md)
-   [**WS\_SECURITY\_PROPERTY**](ws-security-property.md)
-   [**WS\_XML\_SECURITY\_TOKEN\_PROPERTY**](ws-xml-security-token-property.md)

 

 



