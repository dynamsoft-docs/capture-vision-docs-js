---
layout: default-layout
title: Class IdentityUtilityModule - Dynamsoft Barcode Reader JS Edition API Reference
description: This page introduces the IdentityUtilityModule class in Dynamsoft Barcode Reader JS Edition.
keywords: IdentityUtilityModule, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# IdentityUtilityModule Class

This class defines common functionality in the Identity Utility module. At present, it has only one method.

| Name                                 | Description                                          |
| ------------------------------------ | ---------------------------------------------------- |
| `static` [getVersion()](#getversion) | Returns the version of the Identity Utility module.  |

## getVersion

Returns the version of the Identity Utility module.

```typescript
static getVersion(): string;
```

**Return Value**

A string representing the version of the Identity Utility module.

**Code snippet**

```javascript
const version = Dynamsoft.DBR.IdentityUtilityModule.getVersion();
console.log(version);
```

**Remarks**

New added in CaptureVisionBundle version 3.4.2000.