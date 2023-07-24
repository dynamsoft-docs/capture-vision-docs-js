---
layout: default-layout
title: CoreModule Class - Dynamsoft Capture Vision JavaScript Edition
description: This page covers the APIs of the CoreModule Class.
keywords: CoreModule, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: CoreModule Class
permalink: /programming/javascript/api-reference/core/core-module-class.html
---

# CoreModule Class

This class defines common functionality in the `Core` module. At present, it has only one method.

| API Name                           | Description                               |
| ---------------------------------- | ----------------------------------------- |
| static [getVersion()](#getversion) | Returns the version of the `Core` module. |

## getVersion

Returns the version of the `Core` module. 

**Syntax**

```typescript
static getVersion: () => string;
```

**Parameters**

None.

**Return Value**

Returns a string representing the version of the `Core` Module.

**Code snippet**

```javascript
const version = await Dynamsoft.Core.CoreModule.getVersion();
console.log(version);
```
