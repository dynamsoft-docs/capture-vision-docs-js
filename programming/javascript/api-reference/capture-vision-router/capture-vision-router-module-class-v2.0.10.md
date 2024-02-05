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

This class defines common functionality in the CaptureVisionRouter module. At present, it has only one method.

| Name                                          | Description                                                         |
| -------------------------------------------------- | ------------------------------------------------------------------- |
| `static` [getVersion()](#getversion)               | Returns the version of the CaptureVisionRouter module.              |
| `static` [engineResourcePath](#engineresourcepath) | Sets or returns the path to find the resources files (.wasm, etc.). |

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

## engineResourcePath

Sets or returns the path to find the resources files (.wasm, etc.).

**Code snippet**

```javascript
Dynamsoft.CVR.CaptureVisionRouterModule.engineResourcePath = "https://cdn.jsdelivr.net/npm/dynamsoft-capture-vision-router@2.0.30/dist/";