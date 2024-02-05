---
layout: default-layout
title: CaptureVisionRouter Settings - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to the Intermediate-result of CaptureVisionRouter of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, router, Intermediate-result, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: CVR JavaScript CaptureVisionRouter
permalink: /programming/javascript/api-reference/capture-vision-router/intermediate-result.html
---

# CaptureVisionRouter Intermediate Result

| Name                                                            | Description                                                                                |
| --------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| [getIntermediateResultManager()](#getintermediateresultmanager) | Returns an object, of type `IntermediateResultManager`, that manages intermediate results. |

## getIntermediateResultManager

Returns an object, of type `IntermediateResultManager`, that manages intermediate results.

**Syntax**

```typescript
getIntermediateResultManager(): IntermediateResultManager;
```

**Parameters**

None.

**Return Value**

The `IntermediateResultManager` object.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const intermediateResultManager = router.getIntermediateResultManager();
```

**See Also**

[IntermediateResultManager](./intermediate-result-manager.md#intermediateresultmanager)