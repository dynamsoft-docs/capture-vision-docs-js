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

| API Name                                                                                                    | Description                                                                                                                                             |
| ----------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [enableResultCrossVerification()](./multi-frame-result-cross-filter.md#enableresultcrossverification)       | Enables result verification feature to improve the accuracy of video streaming recognition results.                                                     |
| [isResultCrossVerificationEnabled()](./multi-frame-result-cross-filter.md#isresultcrossverificationenabled) | Determines whether the result verification feature is enabled for the specific captured result item type.                                               |
| [enableResultDeduplication()](./multi-frame-result-cross-filter.md#enableresultdeduplication)               | Enables duplicate filter feature to filter out the duplicate results in the period of duplicateForgetTime for video streaming recognition.              |
| [isResultDeduplicationEnabled()](./multi-frame-result-cross-filter.md#isresultdeduplicationenabled)         | Determines whether the duplicate filter feature is enabled for the specific result item type.                                                           |
| [setDuplicateForgetTime()](./multi-frame-result-cross-filter.md#setduplicateforgettime)                     | Sets the duplicate forget time for the specific captured result item types. The same captured result item will be returned only once during the period. |
| [getDuplicateForgetTime()](./multi-frame-result-cross-filter.md#getduplicateforgettime)                     | Gets the duplicate forget time for a specific captured result item type.                                                                                |
