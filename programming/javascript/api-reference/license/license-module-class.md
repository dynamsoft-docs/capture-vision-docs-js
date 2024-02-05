---
layout: default-layout
title: Class LicenseModule - Dynamsoft License Module JS Edition API Reference
description: This page introduces the LicenseModule class in Dynamsoft License Module JS Edition.
keywords: LicenseModule, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---
<!--v3.0.20--Updated on 11/23/2023-->

# LicenseModule Class

This class defines common functionality in the License module. At present, it has only one method.

| Name                            | Description                                |
| ------------------------------------ | ------------------------------------------ |
| `static` [getVersion()](#getversion) | Returns the version of the License module. |

## getVersion

Returns the version of the License module.

```typescript
static getVersion(): string;
```

**Code snippet**

```javascript
const version = Dynamsoft.License.LicenseModule.getVersion();
console.log(version);
```