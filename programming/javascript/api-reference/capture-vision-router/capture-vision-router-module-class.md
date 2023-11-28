---
layout: default-layout
title: Class CaptureVisionRouterModule - Dynamsoft CaptureVisionRouter Module JS Edition API Reference
description: This page introduces the CaptureVisionRouterModule class in Dynamsoft CaptureVisionRouter Module JS Edition.
keywords: CaptureVisionRouterModule, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---
<!-- v2.0.20 -- Updated on 11/28/2023-->

# CaptureVisionRouterModule Class

This class defines common functionality in the CaptureVisionRouter module. At present, it has only one method.

| API Name                             | Description                                            |
| ------------------------------------ | ------------------------------------------------------ |
| `static` [getVersion()](#getversion) | Returns the version of the CaptureVisionRouter module. |

## getVersion

Returns the version of the CaptureVisionRouter module.

```typescript
static getVersion(): string;
```

**Code snippet**

```javascript
const version = Dynamsoft.CaptureVisionRouter.CaptureVisionRouterModule.getVersion();
console.log(version);
```