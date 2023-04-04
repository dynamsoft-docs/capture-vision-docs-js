---
layout: default-layout
title: CaptureVisionRouter Auxiliary APIs - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to the auxiliary APIs of CaptureVisionRouter of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, auxiliary, instance, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
permalink: /programming/javascript/api-reference/cvr/instantiate.html
---

# Javascript API Reference - `CaptureVisionRouter` Instantiation

| API Name                                                      | Description                                                       |
| ------------------------------------------------------------- | ----------------------------------------------------------------- |
| [getIntermediateResultManager](auxiliary.md#) | Whether to save the original image into a &lt;canvas&gt; element. |
| [getVersion](auxiliary.md#getVersion)                         |     

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