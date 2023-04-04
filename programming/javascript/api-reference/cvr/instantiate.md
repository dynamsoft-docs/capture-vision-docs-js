---
layout: default-layout
title: CaptureVisionRouter Instantiation - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to the instantiation of CaptureVisionRouter of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, router, instance, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
permalink: /programming/javascript/api-reference/cvr/instantiate.html
---

# Javascript API Reference - `CaptureVisionRouter` Instantiation

| API Name                            | Description                                                            |
| ----------------------------------- | ---------------------------------------------------------------------- |
| [createInstance()](#createinstance) | Initializes a new instance of the `CaptureVisionRouter` class.         |
| [dispose()](#dispose)               | Releases all resources used by the `CaptureVisionRouter` object.       |
| [disposed](#disposed)               | Returns whether the `CaptureVisionRouter` object has been disposed of. |


## createInstance

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

## dispose

Releases all resources used by the `CaptureVisionRouter` object.

```typescript
dispose: () => void;
```

### Return value

None.

### Code Snippet

```js
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
// Use the router to perform a job.
// ...
// Release the resources after the job is finished.
router.dispose();
```

## disposed

Returns whether the `CaptureVisionRouter` object has been disposed of.

```typescript
disposed: boolean;
```

### Return value

A boolean value that indicates whether the `CaptureVisionRouter` object has been disposed of.

### Code Snippet

```js
if(router.router){
  console.log("The router has been disposed of.");
} else {
  // Use the router to perform a job.
}
```
