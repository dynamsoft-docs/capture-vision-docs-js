---
layout: default-layout
title: CaptureVisionRouter Instantiation - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to the instantiation of CaptureVisionRouter of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, router, instance, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: CVR JavaScript CaptureVisionRouter
permalink: /programming/javascript/api-reference/capture-vision-router/instantiate.html
---

# CaptureVisionRouterInstantiate

| API Name                            | Description                                                            |
| ----------------------------------- | ---------------------------------------------------------------------- |
| [preLoadModule()](#preloadmodule)   | Loads the specified module to speed up the initialization.             |
| [isModuleLoaded()](#ismoduleloaded) | Returns whether the specified module has been loaded.                  |
| [createInstance()](#createinstance) | Initializes a new instance of the `CaptureVisionRouter` class.         |
| [dispose()](#dispose)               | Releases all resources used by the `CaptureVisionRouter` object.       |
| [disposed](#disposed)               | Returns whether the `CaptureVisionRouter` object has been disposed of. |

## preLoadModule

Loads the specified module to speed up the initialization.

**Syntax**

```typescript
preLoadModule(moduleName: string | Array<string>): void
```

**Parameter**

`moduleNameIt`: It takes a string or an array of strings representing the module or modules to preload. Valid values for moduleName are 'DBR' (Dynamsoft Barcode Reader), 'DLR' (Dynamsoft Label Recognizer), 'DDN' (Dynamsoft Document Normalizer), and 'DCP' (Dynamsoft Code Parser).

**Return value**

None.

**Code snippet**

```javascript
Dynamsoft.CVR.CaptureVisionRouter.preloadModule(["DDN"]);
```

## isModuleLoaded

Returns whether the specified module has been loaded.

**Syntax**

```typescript
isModuleLoaded(moduleName: string): boolean;
```

**Parameter**

`moduleName`: It takes a string representing the module to preload. Valid values for moduleName are 'DBR' (Dynamsoft Barcode Reader), 'DLR' (Dynamsoft Label Recognizer), 'DDN' (Dynamsoft Document Normalizer), and 'DCP' (Dynamsoft Code Parser).

**Return value**

A boolean value that indicates whether the required module has been loaded.

**Code snippet**

```javascript
if(router.isModuleLoaded("DDN")){
  // Use the router to perform a DBR job.
} else {
  console.log("DDN module is not preloaded.");
}
```

## createInstance

Initializes a new instance of the `CaptureVisionRouter` class.

**Syntax**

```typescript
createInstance(): Promise<CaptureVisionRouter>;
```

**Parameter**

None.

**Return value**

A promise that resolves to the initialized `CaptureVisionRouter` object.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
```

## dispose

Releases all resources used by the `CaptureVisionRouter` object.

**Syntax**

```typescript
dispose(): Promise<void>;
```

**Parameter**

None.

**Return value**

Returns a promise that resolves when the resources have been successfully released.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
// Use the router to perform a job.
// ...
// Release the resources after the job is finished.
router.dispose();
```

## disposed

Returns whether the `CaptureVisionRouter` object has been disposed of.

**Syntax**

```typescript
disposed: boolean;
```

**Parameter**

None.

**Return value**

A boolean value that indicates whether the `CaptureVisionRouter` object has been disposed of.

**Code snippet**

```javascript
if(router.disposed){
  console.log("The router has been disposed of.");
} else {
  // Use the router to perform a job.
}
```
