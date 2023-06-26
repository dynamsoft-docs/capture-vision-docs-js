---
layout: default-layout
title: CaptureVisionRouter Settings - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to the Intermediate-result of CaptureVisionRouter of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, router, Intermediate-result, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
breadcrumbText: CVR JavaScript CaptureVisionRouter
permalink: /programming/javascript/api-reference/capture-vision-router/intermediate-result.html
---

# Javascript API Reference - Intermediate Result

| API Name                                                      | Description                                               |
| ------------------------------------------------------------- | --------------------------------------------------------- |
| [GetIntermediateResultManager()](#getintermediateresultmanager) | Returns an `CIntermediateResultManager` object.           |

## GetIntermediateResultManager

Returns an object that manages the saving and retrieval of intermediate results.

**Syntax**

```js
getIntermediateResultManager: () => Promise<Core.IntermediateResult.IntermediateResultManager>;
```

**Parameters**

None.

**Return Value**

Returns a promise that resolves with an IntermediateResultManager object.

**Code snippet**

```js
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const intermediateResultManager = await router.getIntermediateResultManager();
// Use the intermediateResultManager to save and retrieve intermediate results
```