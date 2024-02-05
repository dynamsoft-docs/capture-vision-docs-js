---
layout: default-layout
title: Class CaptureVisionRouterModule - Dynamsoft CaptureVisionRouter Module JS Edition API Reference
description: This page introduces the CaptureVisionRouterModule class in Dynamsoft CaptureVisionRouter Module JS Edition.
keywords: CaptureVisionRouterModule, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---
<!-- v2.0.30 -- Updated on 12/19/2023-->

# CaptureVisionRouterModule Class

The `CaptureVisionRouterModule` class defines common functionality in the `CaptureVisionRouter` module.

| Name                                 | Description                                            |
| ------------------------------------ | ------------------------------------------------------ |
| `static` [getVersion()](#getversion) | Returns the version of the CaptureVisionRouter module. |

## getVersion

Returns the version of the CaptureVisionRouter module.

```typescript
static getVersion(): string;
```

**Code snippet**

```javascript
const version = Dynamsoft.CVR.CaptureVisionRouterModule.getVersion();
console.log(version);
```