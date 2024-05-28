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

```typescript
static initLicense(license: string, immediately?: boolean): void | Promise<void>;
```

**Parameters**

`license`: The license key to be used for initialization.

`immediately`: A boolean flag that determines if the function should immediately execute the license initialization or not.

**Return Value**

`void`

* When `immediately` is undefined or false, this signature of `initLicense` passes the license key to the application for initialization at a later stage. It doesn't provide immediate feedback and is suitable for scenarios where immediate confirmation of license initialization is not required.

* When `immediately` is true, this returns a promise that resolves when the operation finishes. It does not provide any value upon resolution. Please note that it may raise up license related exceptions.
  Note - The engineResourcePaths should be set before invoking the init function with true as a parameter. 

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

`name`: A string representing the device which is easier to recognize than its UUID. The maximum length of the string is 255 characters. The null character "\0" is not allowed.

**Return Value**

`void`
