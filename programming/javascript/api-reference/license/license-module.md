---
layout: default-layout
title: API Reference Index - License Module JavaScript Edition
description: This is the index page of the License Module API Reference
keywords: License, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: CVR JavaScript License
permalink: /programming/javascript/api-reference/license/license.html
---

# License Module

The License module is defined in the namespace `Dynamsoft.License`. It consists of the classes `LicenseModule`, `LicenseManager` and the interface `LicenseVerificationListener`.

## LicenseModule Class

This class defines common functionality in the License module. At present, it has only one method.

| API Name                           | Description                                              |
| ---------------------------------- | -------------------------------------------------------- |
| static [getVersion()](#getversion) | Returns the version of the `CaptureVisionRouter` object. |

## LicenseManager Class

The `LicenseManager` class is responsible for the licensing of all functional modules in Dynamsoft Capture Vision architecture.

The APIs for this class are:

| Method                                                                      | Description                                                            |
| --------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| [`getDeviceUUID`](./license-manager.md#getdeviceuuid)                       | Returns the unique identifier of the device.                           |
| [`initLicense`](./license-manager.md#initlicense)                           | Initializes the license using a license key.                           |
| [`setDeviceFriendlyName`](./license-manager.md#setdevicefriendlyname)       | Sets a recognizable name for the device which corresponds to its UUID. |

## LicenseVerificationListener Interface

This interface defines how license verification result is returned.

* [LicenseVerificationListener](./license-verification-listener.md)

## getVersion

Returns the version of the License Module.

**Syntax**

```typescript
static getVersion: () => string;
```

**Parameters**

None.

**Return Value**

Returns a string representing the version of the License Module.

**Code snippet**

```javascript
const version = await Dynamsoft.License.LicenseModule.getVersion();
console.log(version);
```
