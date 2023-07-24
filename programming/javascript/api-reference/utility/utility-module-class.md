---
layout: default-layout
title: API Reference Index - Utility Module JavaScript Edition
description: This is the index page of the Utility Module API Reference
keywords: Utility, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: UtilityModule Class
permalink: /programming/javascript/api-reference/utility/utility-module-class.html
---

# UtilityModule Class

This class defines common functionality in the `Utility` module. At present, it has only one method.

| API Name                           | Description                                  |
| ---------------------------------- | -------------------------------------------- |
| static [getVersion()](#getversion) | Returns the version of the `Utility` module. |

## getVersion

Returns the version of the `Utility` Module.

**Syntax**

```typescript
static getVersion: () => string;
```

**Parameters**

None.

**Return Value**

Returns a string representing the version of the `Utility` Module.

**Code snippet**

```javascript
const version = await Dynamsoft.Utility.UtilityModule.getVersion();
console.log(version);
```
