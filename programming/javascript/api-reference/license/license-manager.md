---
layout: default-layout
title: class LicenseManager - Dynamsoft License Module JS Edition API Reference
description: This page shows the JS edition of the class LicenseManager in Dynamsoft License Module.
keywords: license manager, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LicenseManager

The LicenseManager class provides a set of APIs to manage the licensing for the Dynamsoft Capture Vision architecture.

| API                                               | Description                                                            |
| ------------------------------------------------- | ---------------------------------------------------------------------- |
| [`getDeviceUUID`](#getdeviceuuid)                 | Returns the unique identifier of the device.                           |
| [`initLicense`](#initlicense)                     | Initializes the license using a license key.                           |
| [`setDeviceFriendlyName`](#setdevicefriendlyname) | Sets a recognizable name for the device which corresponds to its UUID. |

## getDeviceUUID

Returns the unique identifier of the device. 

```typescript
static getDeviceUUID(): string;
```

**Return Value**

Returns a string representing the UUID of the device.

## initLicense

Initializes the license using a license key. 

```typescript
static initLicense(license: string): { isSuccess: boolean, error: string };
```

**Parameters**

* `license`: A string representing the license key.

**Return Value**

Returns an object which contains the following information:

* `isSuccess`: indicates whether the license initialization succeeded.
* `error`: specifies what went wrong if `isSuccess` is `false`.

## setDeviceFriendlyName

Sets a recognizable name for the device which corresponds to its UUID.

```typescript
static setDeviceFriendlyName(name: string): void;
```

**Parameters**

`name`: A string representing the device which is easier to recognize than its UUID. 
