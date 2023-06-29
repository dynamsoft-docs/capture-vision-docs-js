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

| Method               | Description |
|----------------------|-------------|
| [`getVersion`](#getversion)                       | Returns the version of the license module.    |
| [`InitLicense`](#initlicense)                     | It is used to initialize the license using a license key. |
| [`SetDeviceFriendlyName`](#setdevicefriendlyname) | It is used to set the friendly name of the device. |
| [`GetDeviceUUID`](#getdeviceuuid)                 | It is used to get the unique identifier of the device. |

### getVersion

### InitLicense

### SetDeviceFriendlyName

### GetDeviceUUID