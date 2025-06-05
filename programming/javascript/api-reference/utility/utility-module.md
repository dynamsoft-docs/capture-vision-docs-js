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

## ImageDrawer Class

The `ImageDrawer` class provides APIs for  for drawing shapes on images.

| Name                                           | Description                                            |
| ---------------------------------------------- | ------------------------------------------------------ |
| [drawOnImage()](./image-drawer.md#drawonimage) | Draws various shapes on an image, and save it in PNG format. |

## ImageIO Class

The `ImageIO` class provides APIs for images reading and saving.

| Name                                        | Description                                            |
| ------------------------------------------- | ------------------------------------------------------ |
| [saveToFile()](./image-io.md#savetofile)         | Saves the specified image in either PNG or JPG format.         |
| [readFromFile()](./image-io.md#readfromfile)     | Reads an image from a file                                     |
| [saveToMemory()](./image-io.md#savetomemory)     | Saves an image to memory.                                      |
| [readFromMemory()](./image-io.md#readfrommemory) | Reads image data from memory using the specified ID.           |

## ImageProcessor Class

The `ImageProcessor` class provides APIs for processing images.

| Name                                        | Description                                            |
| ------------------------------------------- | ------------------------------------------------------ |
| [cropImage()](./image-processor.md#cropimage)                         |  Crops an image using a rectangle or quadrilateral.                                |
| [adjustBrightness()](./image-processor.md#adjustbrightness)           |  Adjusts the brightness of the image.                                              |
| [adjustContrast()](./image-processor.md#adjustcontrast)               |  Adjusts the contrast of the image.                                                |
| [filterImage()](./image-processor.md#filterimage)                     |  Applies a specified image filter to an input image.                               |
| [convertToGray()](./image-processor.md#converttogray)                 |  Converts a colour image to grayscale.                                             |
| [convertToBinaryGlobal()](./image-processor.md#converttobinaryglobal) |  Converts a grayscale image to a binary image using a global threshold.            |
| [convertToBinaryLocal()](./image-processor.md#converttobinarylocal)   |  Converts a grayscale image to a binary image using local (adaptive) binarization. |

## MultiFrameResultCrossFilter Class

The `MultiFrameResultCrossFilter` class provides APIs to configure the filtering of results from multiple images which have been processed consecutively. Usually these images are frames from a streaming video.

| Name                                                                                                        | Description                                                                                  |
| ----------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| [enableLatestOverlapping()](./multi-frame-result-cross-filter.md#enablelatestoverlapping)                   | Enables or disables the to-the-latest overlapping feature of one or multiple specific result item types. This feature can increase the read-rate performance when decoding multiple barcodes under the video streaming. |
| [isLatestOverlappingEnabled()](./multi-frame-result-cross-filter.md#islatestoverlappingenabled)             | Checks if to-the-latest overlapping is active for a given result item type.                  |
| [enableResultCrossVerification()](./multi-frame-result-cross-filter.md#enableresultcrossverification)       | Enables or disables the verification of specific result item types.                          |
| [isResultCrossVerificationEnabled()](./multi-frame-result-cross-filter.md#isresultcrossverificationenabled) | Checks if verification is active for a given result item type.                               |
| [enableResultDeduplication()](./multi-frame-result-cross-filter.md#enableresultdeduplication)               | Enables or disables the deduplication process for specific result item types.                |
| [isResultDeduplicationEnabled()](./multi-frame-result-cross-filter.md#isresultdeduplicationenabled)         | Checks if deduplication is active for a given result item type.                              |
| [setDuplicateForgetTime()](./multi-frame-result-cross-filter.md#setduplicateforgettime)                     | Sets the interval during which duplicates are disregarded for specific result item types.    |
| [getDuplicateForgetTime()](./multi-frame-result-cross-filter.md#getduplicateforgettime)                     | Retrieves the interval during which duplicates are disregarded for a given result item type. |
| [setMaxOverlappingFrames()](./multi-frame-result-cross-filter.md#setmaxoverlappingframes)                   | Set the maximum overlapping frames count for a given result item type.                       |
| [getMaxOverlappingFrames()](./multi-frame-result-cross-filter.md#getmaxoverlappingframes)                   | Get the maximum overlapping frames count for a given result item type.                       |