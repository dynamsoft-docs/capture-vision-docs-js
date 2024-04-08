---
layout: default-layout
title: class LicenseManager - Dynamsoft License Module JS Edition API Reference
description: This page shows the JS edition of the class LicenseManager in Dynamsoft License Module.
keywords: license manager, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---
<!--v3.0.20--Updated on 11/23/2023-->

# LicenseManager

The LicenseManager class provides a set of APIs to manage the licensing for the Dynamsoft Capture Vision architecture.

| API                                                      | Description                                                             |
| -------------------------------------------------------- | ----------------------------------------------------------------------- |
| `static` [getDeviceUUID](#getdeviceuuid)                 | Returns the unique identifier of the device.                            |
| `static` [initLicense](#initlicense)                     | Initializes the license for the application using a license key.        |
| `static` [setDeviceFriendlyName](#setdevicefriendlyname) | Assigns a distinctive name to the device, correlating it with its UUID. |

## getDeviceUUID

Returns the unique identifier of the device.

```typescript
static getDeviceUUID(): Promise<string>;
```

**Return Value**

A promise which, upon resolution, yields a string corresponding to the device's UUID.

## initLicense

Initializes the license for the application using a license key. This function is overloaded, providing two different usages based on the provided parameters.

### Without Immediate Initialization

This signature of `initLicense` passes the license key to the application for initialization at a later stage. It doesn't provide immediate feedback and is suitable for scenarios where immediate confirmation of license initialization is not required.

```typescript
static initLicense(license: string): void;
```

**Parameters**

`license`: The license key to be used for initialization.

**Return Value**

`void`

**Code snippet**

```javascript
Dynamsoft.License.LicenseManager.initLicense("your-license-key");
```

### With Immediate Initialization

This signature of `initLicense` initializes the license and provides immediate feedback through a promise. This is useful when the application needs to confirm the outcome of the license initialization or handle any messages related to it.

```typescript
static initLicense(license: string, immediately: true): Promise<{message?: string} | undefined>;
```

**Parameters**

`license`: The license key to be used for initialization.

`immediately`: A boolean flag that determines if the function should immediately execute the license initialization or not.

**Return Value**

`Promise<{message?: string} | undefined>`

A promise that, upon resolution, yields an object which may include a 'message' property. This property exists if there are messages or notifications pertinent to the license initialization process. In scenarios where no messages exist or if the initialization concludes successfully without any significant conditions, the promise might resolve to 'undefined'.

**Code snippet**

```javascript
Dynamsoft.License.LicenseManager.initLicense("your-license-key", true)
  .then(result => {
    if (result?.message) {
      console.log("License Message:", result.message);
    } else {
      console.log("License initialized successfully");
    }
  })
  .catch(error => {
    console.error("License initialization failed:", error);
  });
```

## setDeviceFriendlyName

Assigns a distinctive name to the device, correlating it with its UUID.

> Please be aware that this method must be called before `Dynamsoft.CVR.CaptureVisionRouter.createInstance()` or `Dynamsoft.Core.CoreModule.loadWasm()` or `Dynamsoft.DCP.CodeParser.createInstance()` to take effect.

```typescript
static setDeviceFriendlyName(name: string): void;
```

**Parameters**

`name`: A string representing the device which is easier to recognize than its UUID. 

**Return Value**

`void`
