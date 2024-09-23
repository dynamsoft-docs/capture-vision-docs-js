---
layout: default-layout
title: DCVB Module Release Notes - Dynamsoft Capture Vision Bundle JavaScript Edition
description:  The release notes of DCVB module - Dynamsoft Capture Vision Bundle JavaScript Edition.
keywords: release notes, capture vision, JavaScript, dcvb
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftCaptureVisionBundle

## 2.2.3000 (00/00/2024)

### DynamsoftCaptureVisionRouter

#### Changed

- Update class CaptureVisionRouter, add new method `getBufferedItemsManager()`.
- Added a new class `BufferedItemsManager` to manage the buffered character items.

#### Fixed

- Fixed the data misalignment issue with point coordinates (x y), compare with C++ version.

### DynamsoftCore

- Added a new error code `EC_PDF_LIBRARY_LOAD_FAILED`.

### DynamsoftBarcodeReader

- Update interfaces `CandidateBarcodeZonesUnit` and `CandidateBarcodeZone` to store the information of a single candidate barcode zone.
- Update interface `LocalizedBarcodesUnit` and `DeformationResistedBarcodeImageUnit` to store the deformation-resisted barcode information.

### DynamsoftLabelRecognizer

#### Highlights

- Added confusable character distinguishing: this feature enhances the library's ability to distinguish between common confusable character sets including {0, o, O}, {1, I, l}, and {5, s, S}, across popular fonts like Arial, Times New Roman, and Verdana, etc.
- Supported confusable character set customization: leveraging the new caching mechanism in the CaptureVisionRouter (CVR) module, the library now enables users to customize confusable character sets to meet the needs of specific scenarios.

#### Changed

- Added new APIs for users to obtain the cached character items and the character clusters:
  - A new interface `BufferedCharacterItemSet` to represent a collection of buffered character items and cluster information.
  - A new interface `BufferedCharacterItem` to represent a basic item of the buffered characters with its image and features information.
  - A new interface `CharacterCluster` to represent a character cluster generated from the collected buffered.

### DynamsoftDocumentNormalizer

#### New

- Added `SimplifiedDocumentNormalizerSettings` to configure basic settings of document processing.
- Added a new enumeration `ImageColourMode` to specify the colour mode of the normalized image.

#### Changed

- Changed the property name from `quadsResultItems` to `detectedQuadResultItems` in interface `DetectedQuadsResult`.

### DynamsoftCameraEnhancer

#### Fixed

* Fixed an issue on iOS 17 where reopening the camera after leaving the browser might fail.

### DynamsoftCodeParser

#### Changed

- Update `loadSpec` to supporting loading multiple specs at a time.

#### Fixed

- Fixed a bug where the same map file is requested more than once.
- Fixed type definition not found issue under TypeScript 5.x version.

### DynamsoftImageProcessing

Separate DynamsoftNeuralNetwork (DNN) part as standalone module.

### DynamsoftNeuralNetwork

The first version of `DynamsoftNeuralNetwork` JavaScript edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.


### DynamsoftLicense

#### Changed

- Change the return type for the method `initLicense`, In case of an error, an exception is thrown.
- Fix wrong path for type definition file in package.json.

### DynamsoftUtility

#### New

- Add method `drawOnImage` for displaying intermediate results on images.

#### Changed

- Improve `MultiFrameResultCrossFilter` to allow `resultItemType` to receive string type parameters.