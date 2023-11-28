---
layout: default-layout
title: API Reference Index - Utility Module JavaScript Edition
description: This is the index page of the Utility Module API Reference
keywords: Utility, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Utility Module
---
<!--v1.0.20--Updated on 11/23/2023-->

# Utility Module

The Utility module is defined in the namespace `Dynamsoft.Utility`. At present, it consists of the classes `UtilityModule`, `ImageManager` and `MultiFrameResultCrossFilter`.

## UtilityModule Class

This class defines common functionality in the Utility module. At present, it has only one method.

| API Name                                                      | Description                                |
| ------------------------------------------------------------- | ------------------------------------------ |
| `static` [getVersion()](./utility-module-class.md#getversion) | Returns the version of the Utility module. |

## ImageManager Class

The `ImageManager` class provides APIs for managing images. At present, it has only one API to save an image as a file.

| API Name                                    | Description                          |
| ------------------------------------------- | ------------------------------------ |
| [saveToFile](./image-manager.md#savetofile) | Saved the specified image as a file. |

## MultiFrameResultCrossFilter Class

The `MultiFrameResultCrossFilter` class provides APIs to configure the filtering of results from multiple images which have been processed consecutively. Usually these images are frames from a streaming video.

* [MultiFrameResultCrossFilter](./multi-frame-result-cross-filter.md)
