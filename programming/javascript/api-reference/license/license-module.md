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

The License module is defined in the namespace `Dynamsoft.License`. It consists of the classes `LicenseModule`, `LicenseManager` and the interface `LicenseVerificationListener`.

## LicenseModule Class

This class defines common functionality in the `License` module. At present, it has only one method.

| API Name                                                  | Description                                  |
| --------------------------------------------------------- | -------------------------------------------- |
| static [getVersion()](license-module-class.md#getversion) | Returns the version of the `License` module. |

## LicenseManager Class

The `LicenseManager` class is responsible for the licensing of all functional modules in Dynamsoft Capture Vision architecture.

The APIs for this class are:

| Method                                                                | Description                                                            |
| --------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| [`getDeviceUUID`](./license-manager.md#getdeviceuuid)                 | Returns the unique identifier of the device.                           |
| [`initLicense`](./license-manager.md#initlicense)                     | Initializes the license using a license key.                           |
| [`setDeviceFriendlyName`](./license-manager.md#setdevicefriendlyname) | Sets a recognizable name for the device which corresponds to its UUID. |

## LicenseVerificationListener Interface

This interface defines how license verification result is returned.

* [LicenseVerificationListener](./license-verification-listener.md)
