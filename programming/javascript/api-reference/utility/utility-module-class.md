---
layout: default-layout
title: Class UtilityModule - Dynamsoft Utility Module JS Edition API Reference
description: This page introduces the UtilityModule class in Dynamsoft Utility Module JS Edition.
keywords: UtilityModule, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---
<!--v1.0.20 -- added  on 11/28/2023-->

# UtilityModule Class

This class defines common functionality in the Utility module. At present, it has only one method.

| Name                            | Description                                |
| ------------------------------------ | ------------------------------------------ |
| `static` [getVersion()](#getversion) | Returns the version of the Utility module. |

## getVersion

Returns the version of the Utility module.

```typescript
static getVersion(): string;
```

**Code snippet**

```javascript
const version = Dynamsoft.Utility.UtilityModule.getVersion();
console.log(version);
```
