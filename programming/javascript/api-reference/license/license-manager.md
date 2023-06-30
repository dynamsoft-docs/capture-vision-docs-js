---
layout: default-layout
title: class LicenseManger - Dynamsoft License Module JS Edition API Reference
description: This page shows the JS edition of the class LicenseManger in Dynamsoft License Module.
keywords: license manager, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LicenseManager

The LicenseManager class provides a set of APIs to manage SDK licensing.

## Definition

```js
export class LicenseManager {
            static DYNAMSOFT_LICENSE_VERSION: string = "3.0.0";
            static initLicense: (license: string) => Promise<LicenseVerificationListener>;
            static setDeviceFriendlyName: (name: string) => void;
            static getDeviceUUID: () => string;
        } 
```

## Methods Summary

| Method & Attribute       | Description |
|----------------------|-------------|
| [`DYNAMSOFT_LICENSE_VERSION`](#dynamsoftlicenseversion)        | Returns the version of the license module.   |
| [`InitLicense`](#initlicense)                     | It is used to initialize the license using a license key. |
| [`SetDeviceFriendlyName`](#setdevicefriendlyname) | It is used to set the friendly name of the device. |
| [`GetDeviceUUID`](#getdeviceuuid)                 | It is used to get the unique identifier of the device. |

### DYNAMSOFT_LICENSE_VERSION

A string represents the version of the license module.

```js
static DYNAMSOFT_LICENSE_VERSION: string = "3.0.0";
```

### InitLicense

It is used to initialize the Dynamsoft license.

```js
static initLicense: (license: string) => Promise<LicenseVerificationListener>;
```

**Parameters**

`license`: A string representing the license key.

**Return Value**

Returns a promise that resolves to a `LicenseVerificationListener`. The `LicenseVerificationListener` is an interface that provides callbacks for license verification status.

### SetDeviceFriendlyName

It is used to set the friendly name for the device.

```js
static setDeviceFriendlyName: (name: string) => void;
```

**Parameters**

`name`: A string representing the friendly name of the device.

### GetDeviceUUID

It is used to get the Universally Unique Identifier (UUID) of the device.

```js
static getDeviceUUID: () => string;
```

**Return Value**

Returns a string representing the UUID of the device.
