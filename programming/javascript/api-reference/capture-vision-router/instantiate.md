---
layout: default-layout
title: CaptureVisionRouter Instantiation - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to the instantiation of CaptureVisionRouter of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, router, instance, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: CVR JavaScript CaptureVisionRouter
---

# CaptureVisionRouter Instantiate

| Name                                         | Description                                                              |
| -------------------------------------------- | ------------------------------------------------------------------------ |
| `static` [createInstance()](#createinstance) | Initializes a new instance of the `CaptureVisionRouter` class.           |
| [dispose()](#dispose)                        | Releases all resources used by the `CaptureVisionRouter` instance.       |
| [disposed](#disposed)                        | Returns whether the `CaptureVisionRouter` instance has been disposed of. |

## createInstance

Initializes a new instance of the `CaptureVisionRouter` class.

**Syntax**

```typescript
createInstance(): Promise<CaptureVisionRouter>;
```

**Parameter**

None.

**Return value**

A promise that resolves to the initialized `CaptureVisionRouter` instance.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
```

## dispose

Releases all resources used by the `CaptureVisionRouter` instance.

**Syntax**

```typescript
dispose(): Promise<void>;
```

**Parameter**

None.

**Return value**

A promise that resolves when the resources have been successfully released.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
// Use the router to perform a job.
// ...
// Release the resources after the job is finished.
router.dispose();
```

## disposed

Returns whether the `CaptureVisionRouter` instance has been disposed of.

**Syntax**

```typescript
disposed: boolean;
```

**Parameter**

None.

**Return value**

Boolean indicating whether the `CaptureVisionRouter` instance has been disposed of.

**Code snippet**

```javascript
if(router.disposed){
    console.log("The router has been disposed of.");
} else {
    // Use the router to perform a job.
}
```