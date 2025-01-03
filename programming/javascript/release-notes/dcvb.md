---
layout: default-layout
title: DCVB Module Release Notes - Dynamsoft Capture Vision Bundle JavaScript Edition
description:  The release notes of DCVB module - Dynamsoft Capture Vision Bundle JavaScript Edition.
keywords: release notes, capture vision, JavaScript, dcvb
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftCaptureVisionBundle

## 2.6.1000 (01/03/2025)

### Highlights

- Enhanced document detection delivers more reliable results, particularly for single-document scenarios. Key improvements include:
  - Strengthened detection algorithms for greater accuracy and robustness.
  - Optimized parameter configurations for better adaptability across diverse scenarios.
  - Refined cross-verification rules to ensure more consistent detection outcomes.
- Introduced a feature to track and accumulate recognized barcodes across multiple frames in real-time video, enabling seamless multi-barcode recognition.

### Changelogs

#### New

- Added a new mode, `CICM_EDGE_ENHANCEMENT`, to the `ColourConversionModes` parameter, designed to enhance edge details when converting a color image to grayscale.
- Introduced the concept of `LogicLines` to enhance the processing and analysis of document structures.
  - Added a new value, `IRUT_LOGIC_LINES`, to the `IntermediateResultUnitType` enumeration.
  - Added a new function `onLogicLinesReceived` to the class `IntermediateResultReceiver` which will be called when logic lines have been received.
  - Added a new class, `LogicLinesUnit`, to represent an intermediate result unit containing logic lines.
- Added the `getCrossVerificationStatus` function to both the `DetectedQuadResultItem` and `NormalizedImageResultItem` classes, along with a new `EnumCrossVerificationStatus` enumeration, to retrieve the cross-verification status of the result.
- Added the `getParameterTemplateCount` and `getParameterTemplateName` functions to the `CaptureVisionRouter` class to improve accessibility and usability of templates.
- Added to-the-latest overlapping feature. You can use `enableLatestOverlapping` function of `MultiFrameResultCrossFilter` class to enable this feature.
- Added the `getFieldRawValue` method to the `ParsedResultItem` class to retrieve the raw value of the field.

#### Fixed

- Fixed a bug in `TextZone` caused by the absence of a custom copy constructor, which led to improper memory management with the default copy constructor.
- Fixed a bug in DPM mode where the `isMirrored` value in the `BarcodeResultItem` was not correctly assigned.
- Fixed a bug where DotCode could not be decoded in certain scenarios.
- Small fixes and tweaks.
  
#### Changed

- Updated the parameter configurations for the `DetectDocumentBoundaries_Default` and `DetectAndNormalizeDocument_Default` preset templates to default to single-document mode.
- Changed default value of `ExpectedDocumentsCount` parameter from 0 to 1 to better support single-document mode.
- Changed default value of `CornerAngleRange` parameter from [70, 110] to [60, 120] to support a wider range of document capture angles.
- Modified the return logic for `DetectedQuadResultItem` and `NormalizedImageResultItem` when `ResultCrossVerification` is `enabled`. Previously, only verified results were returned; now, results are returned regardless of verification status, and the results include a `CrossVerificationStatus` to indicate the verification state.
- Removed the `LineExtractionModes` parameter and replaced it with `ShortlineDetectionMode` and `LineAssemblyMode` for more flexible and precise configuration.

## 2.4.2200 (10/24/2024)

### Highlights

- Improved the read rate and the speed of the following barcode formats:
  - EAN13
  - DotCode
- Added support for decoding add-on codes (also known as Extension Codes) for UPC-A, UPC-E, EAN-8 and EAN-13 codes.

### DynamsoftCaptureVisionRouter

#### Improved

- Updated the error handling logic of `capturing` & `startCapturing` methods. The methods will be able to clearly report where the error occurred if the capturing fails due to an licensing issue.

#### New

- Added internal logics for usage count.
- Added a new callback function `OnRawTextLinesReceived` to the class `IntermediateResultReceiver`.
- Add `EnumPresetTemplate` for all preset template names

### DynamsoftCore

#### Improved

- Updated the path auto-filling mechanism to reduce non-essential path definitions.

#### New

- Added new error codes
  - -10076: The license is initialized successfully but detected invalid content in your key.
  - -30063: [Barcode Reader] No license found.
  - -40103: [Label Recognizer] No license found.
  - -50058: [Document Normalizer] No license found.
  - -90012: [Code Parser] No license found.
- Added a new enumeration member `IRUT_RAW_TEXT_LINES` to the `EnumIntermediateResultUnitType`.

### DynamsoftLicense

#### Improved

- Updated the error message of `initLicense` method. The methods will returns more detailed messages when failed to initialized the license. Warnings will be available if license initialization is successful but a part of the license key is invalid.
- Updated the duplicate license error handling mechanism. After successfully creating an instance, setting the same license again will no longer cause exception.

#### New

- Add a new charge way, `TimeSliceCount`.

### DynamsoftImageProcessing

#### Fixed

- Fixed a crash bug caused by the usage of RegEx.
- Small fixes and tweaks.

### DynamsoftUtility

#### Fixed

- Fixed a bug where `CaptureVisionRouter.startCapturing` would erroneously halt the fetching process when its status was running, leading to an unnecessary stop and restart of the fetching operation.

### DynamsoftBarcodeReader

#### Improved

- Improved the read rate and the speed of the following barcode formats:
  - EAN13
  - DotCode

#### New

- Added internal logics for usage count.
- Added support for decoding add-on barcodes.
- Added new properties to the `QRCodeDetails` class
  - `dataMaskPattern`
  - `codewords`

#### Changed

- Updated the Enumeration number of `EnumBarcodeFormat.BF_ALL` to 0xFFFFFFFEFFFFFFFF.
- Updated the internal logic of licensing error message reporting.

#### Fixed

- Fixed a bug that might cause `GS1_DATABAR_EXPANDED_STACKED` barcode unread.

### DynamsoftLabelRecognizer

#### New

- Added internal logics for usage count.
- Added a new parameter CharSet to the `CharacterModel` object to include or exclude characters for recognition.
- Added a new algorithm stage `IRUT_RAW_TEXT_LINES`.  Corresponding APIs are added to obtain the intermediate result of this stage.
  - Interface `RawTextLinesUnit`
  - Interface `RawTextLine`
  - Enumeration `RawTextLineStatus`
- Added a property `rawText` to the interface `RecognizedTextLineELement`.
- Added a property `rawText` to the interface `TextLineResultItem`.

### DynamsoftNocumentNormalizer

#### New

- Added a new parameter `MinDocumentAreaRatio` to define the minimum targeting document area. The parameter is available via both the parameter template and the `SimplifiedDocumentNormalizerSettings`.
- Added a new parameter `ExpectedDocumentsCount` to define the expected document count for detection. The parameter is available via both the parameter template and the `SimplifiedDocumentNormalizerSettings`.

#### Changes

- Updated internal logics to to use the latest version of `DynamsoftCore` module.

#### Fixed

- Small fixes and tweaks.

### DynamsoftCodeParser

#### Fixed

- Fixed a bug where the South African Driver's license might be parsed incorrectly.

#### Changed

- Updated the internal logic of licensing error message reporting.

### DynamsoftCameraEnhancer

#### New

- A new preset UI template has been added, which is available for use and modification.

## 2.2.3000 (07/21/2024)

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