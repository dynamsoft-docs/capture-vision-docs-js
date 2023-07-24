---
layout: default-layout
title: LicenseModule Class - Dynamsoft Capture Vision JavaScript Edition
description: This page covers the APIs of the LicenseModule Class.
keywords: LicenseModule, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: LicenseModule Class
permalink: /programming/javascript/api-reference/license/license-module-class.html
---

# LicenseModule Class

This class defines common functionality in the `License` module. At present, it has only one method.

| API Name                           | Description                                  |
| ---------------------------------- | -------------------------------------------- |
| static [getVersion()](#getversion) | Returns the version of the `License` module. |

## getVersion

Returns the version of the `License` module. 

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
