---
layout: default-layout
title: API Reference Index - License Module JavaScript Edition
description: This is the index page of the License Module API Reference
keywords: License, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: License Module
---
<!--v3.0.20--Updated on 11/23/2023-->

# DynamsoftLicense Module

The License module is defined in the namespace `Dynamsoft.License`. It consists of the classes `LicenseModule` and `LicenseManager`.

## LicenseModule Class

This class defines common functionality in the License module. At present, it has only one method.

| Name                                                     | Description                                |
| ------------------------------------------------------------- | ------------------------------------------ |
| `static` [getVersion()](./license-module-class.md#getversion) | Returns the version of the License module. |

## LicenseManager Class

The `LicenseManager` class is responsible for the licensing of all functional modules in Dynamsoft Capture Vision architecture.

The APIs for this class are:

| API                                                                          | Description                                                             |
| ---------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `static` [getDeviceUUID](./license-manager.md#getdeviceuuid)                 | Returns the unique identifier of the device.                            |
| `static` [initLicense](./license-manager.md#initlicense)                     | Initializes the license for the application using a license key.        |
| `static` [setDeviceFriendlyName](./license-manager.md#setdevicefriendlyname) | Assigns a distinctive name to the device, correlating it with its UUID. |