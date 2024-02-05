---
layout: default-layout
title: DCE Module Release Notes - Dynamsoft Capture Vision JavaScript Edition
description: The release notes of DynamsoftCameraEnhancer module - Dynamsoft Capture Vision JavaScript Edition.
keywords: release notes, camera enhancer, JavaScript, DCE
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftCameraEnhancer Module

## 4.0.1 (01/11/2024)

### Added

* Added `beepSoundSource` & `vibrateDuration` to the class `Feedback`.
* Added `maintainAspectRatio` to `ImageDrawingItem`.
* Added `clearAllInnerDrawingItems()` to clear internally added DrawingItems.
* Added `setErrorListener()` to receive errors occurred during image acquisition.
* Added `cameraOpenTimeout` to control the maximum time allowed for opening a selected camera.

### Improved

* Updated the behaviour of `SingleFrameMode` to allow an JavaScript or iOS device user to make use of the camera without having to select between the camera and image gallery as the image source. 
* Updated the method `setScanRegion()` to allow passing `null` to clear the scan region.
* Updated the resolution selection drop-down box to make it more intuitive.
* Updated `setZoom()` to support Safari on iOS v17.x.

### Fixed

* Fixed issues with the methods `setZoom()` & `getZoomSettings()` so that they can now work with static videos.
* Fixed issues with the autozoom or enhanced-focus features to prevent them from throwing unnecessary error messages.
* Fixed an issue with unstable video streaming upon opening the camera on iOS 17.x.

## 4.0.0 (08/24/2023)

The first version of `DynamsoftCameraEnhancer(DCE)` JavaScript edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.
