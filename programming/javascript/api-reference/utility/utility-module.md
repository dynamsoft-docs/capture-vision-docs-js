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

The `Utility` module is defined in the namespace `Dynamsoft.Utility`. At present, it consists of the classes `UtilityModule`, `ImageManager` and the interface `MultiFrameResultCrossFilter`.

## UtilityModule Class

This class defines common functionality in the Utility module. At present, it has only one method.

| API Name              | Description                                  |
| --------------------- | -------------------------------------------- |
| static `getVersion()` | Returns the version of the `Utility` module. |

**Code snippet**

```javascript
const version = await Dynamsoft.Utility.UtilityModule.getVersion();
console.log(version);
```

## ImageManager Class

The `ImageManager` class provides APIs for managing images. At present, it has only one API to save an image as a file.

The APIs for this class are:

| API Name                                    | Description                          |
| ------------------------------------------- | ------------------------------------ |
| [`saveToFile`](image-manager.md#savetofile) | Saved the specified image as a file. |

## MultiFrameResultCrossFilter Interface

This interface defines how license verification result is returned.

* [MultiFrameResultCrossFilter](./multi-frame-result-cross-filter.md)
