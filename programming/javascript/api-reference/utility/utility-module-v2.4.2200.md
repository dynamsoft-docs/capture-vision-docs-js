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

# DynamsoftUtility Module

The Utility module is defined in the namespace `Dynamsoft.Utility`. At present, it consists of the classes `UtilityModule`, `ImageManager` and `MultiFrameResultCrossFilter`.

## UtilityModule Class

This class defines common functionality in the Utility module. At present, it has only one method.

| Name                                                          | Description                                |
| ------------------------------------------------------------- | ------------------------------------------ |
| `static` [getVersion()](./utility-module-class.md#getversion) | Returns the version of the Utility module. |

## ImageManager Class

The `ImageManager` class provides APIs for managing images. At present, it has only one API to save an image as a file.

| Name                                        | Description                                            |
| ------------------------------------------- | ------------------------------------------------------ |
| [saveToFile](./image-manager.md#savetofile) | Saves the specified image in either PNG or JPG format. |

## MultiFrameResultCrossFilter Class

The `MultiFrameResultCrossFilter` class provides APIs to configure the filtering of results from multiple images which have been processed consecutively. Usually these images are frames from a streaming video.

| Name                                                                                                        | Description                                                                                  |
| ----------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| [enableResultCrossVerification()](./multi-frame-result-cross-filter.md#enableresultcrossverification)       | Enables or disables the verification of specific result item types.                          |
| [isResultCrossVerificationEnabled()](./multi-frame-result-cross-filter.md#isresultcrossverificationenabled) | Checks if verification is active for a given result item type.                               |
| [enableResultDeduplication()](./multi-frame-result-cross-filter.md#enableresultdeduplication)               | Enables or disables the deduplication process for specific result item types.                |
| [isResultDeduplicationEnabled()](./multi-frame-result-cross-filter.md#isresultdeduplicationenabled)         | Checks if deduplication is active for a given result item type.                              |
| [setDuplicateForgetTime()](./multi-frame-result-cross-filter.md#setduplicateforgettime)                     | Sets the interval during which duplicates are disregarded for specific result item types.    |
| [getDuplicateForgetTime()](./multi-frame-result-cross-filter.md#getduplicateforgettime)                     | Retrieves the interval during which duplicates are disregarded for a given result item type. |