---
layout: default-layout
title: API Reference Index - License Module JavaScript Edition
description: This is the index page of the License Module API Reference
keywords: License, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: License Module
permalink: /programming/javascript/api-reference/license/license-module.html
---

# License Module

The License module is defined in the namespace `Dynamsoft.License`. It consists of the classes `LicenseModule` and `LicenseManager`.

## LicenseModule Class

This class defines common functionality in the `License` module. At present, it has only one method.

| API Name              | Description                                  |
| --------------------- | -------------------------------------------- |
| static `getVersion()` | Returns the version of the `License` module. |

**Code snippet**

```javascript
const version = Dynamsoft.License.LicenseModule.getVersion();
console.log(version);
```

## LicenseManager Class

The `LicenseManager` class is responsible for the licensing of all functional modules in Dynamsoft Capture Vision architecture.

The APIs for this class are:

| API Name                                                                     | Description                                                            |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| static [`getDeviceUUID`](./license-manager.md#getdeviceuuid)                 | Returns the unique identifier of the device.                           |
| static [`initLicense`](./license-manager.md#initlicense)                     | Initializes the license using a license key.                           |
| static [`setDeviceFriendlyName`](./license-manager.md#setdevicefriendlyname) | Sets a recognizable name for the device which corresponds to its UUID. |
