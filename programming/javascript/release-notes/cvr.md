---
layout: default-layout
title: CVR Module Release Notes - Dynamsoft Capture Vision JavaScript Edition
description:  The release notes of CaptureVisionRouter module - Dynamsoft Capture Vision JavaScript Edition.
keywords: release notes, capture vision router, JavaScript, cvr
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - CaptureVisionRouter Module

## 2.2.30 (05/15/2024)

### Changed

- Updated the capture vision router algorithm to v2.2.30, see[CaptureVisionRouter C++ v2.2.30](https://www.dynamsoft.com/capture-vision/docs/server/programming/cplusplus/release-notes/cvr.html#2230-0513) for more details.
  - Update class CaptureVisionRouter, add new method `getBufferedItemsManager()`.
  - Added a new class `BufferedItemsManager` to manage the buffered character items.

### Fixed

- Fixed the data misalignment issue with point coordinates (x y), compare with C++ version.

## 2.2.10 (04/11/2024)

- Updated the capture vision router algorithm to v2.2.10, see[CaptureVisionRouter C++ v2.2.10](https://www.dynamsoft.com/capture-vision/docs/server/programming/cplusplus/release-notes/cvr.html#2210-0301) for more details.
- Move the interface `CapturedResult` from Core to CVR.
- Update `SimplifiedCaptureVisionSettings` to support `SimplifiedDocumentNormalizerSettings`.
- Update `IntermediateResultReceiver` to add call back function `onShortLinesUnitReceived()` and method `getObservationParameters`.
- Small fixes and tweaks.

## 2.0.32 (02/01/2024)

### Fixed

- Fixed a bug where the intermediate result callback function was not triggered in single frame mode.
- Fixed a type error bug encountered when utilizing `CapturedResultReceiver` or `CapturedResultFilter` in a TypeScript environment.

## 2.0.31 (01/29/2024)

### Changed

- Rename the method name to `OnImageSourceStateReceived` under interface `ImageSourceStateListener`.
- Removed redundant 's' from the middle of property names 'barcodesResultItems,' 'quadsResultItems,' and 'textLinesResultItems in various result classes to maintain consistent naming with C++ edition.

## 2.0.30 (01/11/2024)

### New

Updated the capture vision router algorithm to v2.0.30, see[CaptureVisionRouter C++ v2.0.30](https://www.dynamsoft.com/capture-vision/docs/server/programming/cplusplus/release-notes/cvr.html#2030-02012024) for more details.

### Break Changes

- The following classes are migrated from DynamsoftCore module:
  - CIntermediateResultReceiver
  - CapturedResultReceiver
  - CapturedResultFilter
  - CIntermediateResultManager

## 2.0.11 (08/24/2023)

The first version of `DynamsoftCaptureVisionRouter` JavaScript edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.
