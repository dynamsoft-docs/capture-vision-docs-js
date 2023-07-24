---
layout: default-layout
title: API Reference Index - Utility Module JavaScript Edition
description: This is the index page of the Utility Module API Reference
keywords: Utility, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Utility Module
permalink: /programming/javascript/api-reference/utility/utility-module.html
---

# Utility Module

The Utility module is defined in the namespace `Dynamsoft.Utility`. It consists of the classes `ImageManager` and the interface `MultiFrameResultCrossFilter`.

## UtilityModule Class

This class defines common functionality in the Utility module. At present, it has only one method.

| API Name                           | Description                                  |
| ---------------------------------- | -------------------------------------------- |
| static [getVersion()](#getversion) | Returns the version of the `Utility` module. |

## ImageManager Class

The `LicenseManager` class is responsible for the licensing of all functional modules in Dynamsoft Capture Vision architecture.

The APIs for this class are:

| Method                                                                | Description                                                            |
| --------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| [`getDeviceUUID`](./license-manager.md#getdeviceuuid)                 | Returns the unique identifier of the device.                           |
| [`initLicense`](./license-manager.md#initlicense)                     | Initializes the license using a license key.                           |
| [`setDeviceFriendlyName`](./license-manager.md#setdevicefriendlyname) | Sets a recognizable name for the device which corresponds to its UUID. |

## MultiFrameResultCrossFilter Interface

This interface defines how license verification result is returned.

* [LicenseVerificationListener](./license-verification-listener.md)

## getVersion

Returns the version of the Utility Module.

**Syntax**

```typescript
static getVersion: () => string;
```

**Parameters**

None.

**Return Value**

Returns a string representing the version of the Utility Module.

**Code snippet**

```javascript
const version = await Dynamsoft.Utility.LicenseModule.getVersion();
console.log(version);
```
