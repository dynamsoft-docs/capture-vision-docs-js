---
layout: default-layout
title: CaptureVisionRouter Module Class - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs of the CaptureVisionRouterModule class of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, module, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: CaptureVisionRouter Module Class
permalink: /programming/javascript/api-reference/capture-vision-router/capture-vision-router-module-class.html
---

## CaptureVisionRouterModule Class

This class defines common functionality in the `CaptureVisionRouter` module. At present, it has only one method.

| API Name                           | Description                                              |
| ---------------------------------- | -------------------------------------------------------- |
| static [getVersion()](#getversion) | Returns the version of the `CaptureVisionRouter` object. |

## getVersion

Returns the version of the CaptureVisionRouter Module.

**Syntax**

```typescript
static getVersion: () => string;
```

**Parameters**

None.

**Return Value**

Returns a string representing the version of the `CaptureVisionRouter` module.

**Code snippet**

```javascript
const version = await Dynamsoft.CVR.CaptureVisionRouterModule.getVersion();
console.log(version);
```
