---
layout: default-layout
title: CaptureVisionRouter Auxiliary APIs - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to the auxiliary APIs of CaptureVisionRouter of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, auxiliary, instance, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
permalink: /programming/javascript/api-reference/capture-vision-router/auxiliary.html
---

# Javascript API Reference - Auxiliary Methods

| API Name                                                      | Description                                              |
| ------------------------------------------------------------- | -------------------------------------------------------- |
| [getIntermediateResultManager](#getintermediateresultmanager) | Returns an `IntermediateResultManager` object.           |
| [getVersion](#getversion)                                     | Returns the version of the `CaptureVisionRouter` object. |

## getIntermediateResultManager

Initializes a new instance of the `CaptureVisionRouter` class.

```typescript
Dynamsoft.CVR.CaptureVisionRouter.createInstance: () => Promise<CaptureVisionRouter>;
```

### Return value

A promise that resolves to the initalized `CaptureVisionRouter` object.

### Code Snippet

```js
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
```

## getVersion