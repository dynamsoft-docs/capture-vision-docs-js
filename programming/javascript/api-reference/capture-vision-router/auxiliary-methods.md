---
layout: default-layout
title: CaptureVisionRouter Auxiliary APIs - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to the auxiliary APIs of CaptureVisionRouter of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, auxiliary, instance, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: CVR JavaScript CaptureVisionRouter
permalink: /programming/javascript/api-reference/capture-vision-router/auxiliary-methods.html
---

# Javascript API Reference - Auxiliary Methods

| API Name                                                      | Description                                              |
| ------------------------------------------------------------- | -------------------------------------------------------- |
| [getVersion()](#getversion)                                     | Returns the version of the `CaptureVisionRouter` object. |

## getVersion

Returns the version of the CaptureVisionRouter.

**Syntax**

```ts
static getVersion: () => string;
```

**Parameters**

None.

**Return Value**

Returns a string representing the version of the CaptureVisionRouter.

**Code snippet**

```ts
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const version = CaptureVisionRouter.getVersion();
console.log(version);
```