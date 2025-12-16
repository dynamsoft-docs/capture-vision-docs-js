---
layout: default-layout
title: DCVB Release Notes v3.x - Dynamsoft Capture Vision Bundle JavaScript Edition
description:  The release notes of DCVB v3.x - Dynamsoft Capture Vision Bundle JavaScript Edition.
keywords: release notes, capture vision, JavaScript, dcvb, 3.x
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftCaptureVisionBundle

## 3.2.5000 (12/16/2025)

This release includes security maintenance updates to ensure continued protection of the product.

### Security Updates

- Updated third-party libraries to incorporate the latest security fixes.

## 3.2.4000 (11/11/2025)

### Fixed

- Fixed a bug that could cause a crash when using model localization with a 2D barcode.

## 3.2.2000 (11/04/2025)

### 🎉Milestone Release
Version 3.2.2000 introduces a series of AI-driven improvements designed to enhance barcode and MRZ detection accuracy, processing speed, and configuration flexibility.

This release focuses on practical performance gains for production environments across retail, logistics, manufacturing, and identity verification workflows.

### ✨ Key Highlights
#### AI-Powered Barcode Detection and Decoding

- New Localization Models – Introduces [`OneDLocalization`]({{ site.dcvb_parameters }}barcode-reader-task-settings/localization-modes.html#modelnamearray) and [`DataMatrixQRCodeLocalization`]({{ site.dcvb_parameters }}barcode-reader-task-settings/localization-modes.html#modelnamearray) neural network models for improved detection of **blurred / low-resolution 1D codes**, or **partially damaged DataMatrix/QR codes**.
- Specialized Decoders – Adds [`EAN13Decoder`]({{ site.dcvb_parameters }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) and [`Code128Decoder`]({{ site.dcvb_parameters }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) models optimized for **long-distance** and **motion-blurred** decoding scenarios.
- Redesigned Deblur Model – The [`OneDDeblur`]({{ site.dcvb_parameters }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) model now provides more effective recovery from **motion and focus blur**.
- Configurable Model Selection – The new `ModelNameArray` parameter supports flexible model loading and fine-grained control for specific barcode types.

#### Precision and Processing Control

- Enhanced Deblur Methods – [`DM_DEEP_ANALYSIS`]({{ site.dcvb_parameters }}barcode-reader-task-settings/deblur-modes.html#dm_deep_analysis) now includes sub-level control with `OneDGeneral`, `TwoDGeneral`, and `EAN13Enhanced` options.
- Barcode Count Expectation – The new [`ExpectedBarcodesCount`]({{ site.dcvb_parameters }}barcode-format-specification/expected-barcodes-count.html) parameter enables **format-specific quantity control** and **early termination** in fixed-count workflows.
- Improved Region Detection – The new [`RPM_GRAY_CONSISTENCY`]({{ site.dcvb_parameters }}image-parameter/region-predetection-modes.html#rpm_gray_consistency) mode provides more precise region extraction based on **grayscale uniformity** and **local consistency** for document and label processing.

#### AI-Powered MRZ Detection

- Neural MRZ Localization – The new [`MRZLocalization`]({{ site.dcvb_parameters }}label-recognizer-task-settings/localization-modes.html#modelnamearray) model improves region detection accuracy and delivers up to **42.7%** faster processing for MRZ-based document workflows.
- Configurable Localization Control – The new [`LocalizationModes`]({{ site.dcvb_parameters }}label-recognizer-task-settings/localization-modes.html) parameter allows configuration for text line detection.

### Performance Highlights

#### Barcode Workflows

- Up to **26.5%** higher read rates under blur conditions with as much as **44%** faster processing.
- Reliable decoding of DataMatrix and QR codes with missing or damaged finder patterns.
- Extended operational range beyond 75 cm for long-distance barcode scanning.

### Developer Notes

- Backward Compatibility – Fully compatible with existing integrations; no code-level changes required for upgrade.
- Configuration Flexibility – Expanded parameter set allows comprehensive model configuration for scenario-specific tuning.
- Production Stability – All new models validated in enterprise environments.

## API Changes

### New

- Added the `switchCapturingTemplate()` method to the `CaptureVisionRouter` class to enable switching the active capturing template during the image processing workflow. 
- Added methods `toBlob()`, `toImage()`, and `toCanvas()` to the `originalImageResultItem` interface for flexible image data conversion.
- Added the `SetGlobalIntraOpNumThreads()` method to the `CaptureVisionRouter` class to configure the global thread count for model inference.  
- Added the `clearDLModelBuffers()` method to the `CaptureVisionRouter` class to manually release memory occupied by loaded models.  
- Added callback functions `onSpecLoadProgressChanged()` and `onWasmLoadProgressChanged()` to monitor resource loading progress.  
- Added the `convertToContainCoordinates()` method to the `CameraEnhancer` class to convert coordinates from `fit: cover` to `fit: contain` mode.  
- Added the `LM_NEURAL_NETWORK` enumeration to `EnumLocalizationMode`.  

### Updated

- Changed the default value of `MaxThreadsInOneTask` from **4** to **0**.  
- Changed the default value of `IncludeTrailingCheckDigit` from **1** to **0**.  

### Deprecated

- Deprecated the `DeblurModelNameArray` argument in the `DeblurModes` parameter. Use `ModelNameArray` instead.  
- Deprecated the `appendModelBuffer()` method in the `CaptureVisionRouter` class. Use `appendDLModelBuffer()` instead.  

## 3.0.6001(08/28/2025)

### Fixed

- Rebuilt the WASM file to resolve a performance degradation issue.
- Added back missing type definitions for `documentSettings` and `labelSettings`.

## 3.0.6000(08/14/2025)

### New

- **Base64 String Conversion**: Enabled bidirectional conversion between `ImageData` and Base64 strings.

- **Template Version Validation**: Introduced version checking for templates to prevent compatibility issues and mismatches.

### Improved

- **White-on-White Document Recognition**: Optimized accuracy for document detection in scenarios where white paper is placed on a white background.

### Changed

- **License Validation Behavior**: Instead of stopping execution immediately on an invalid license module, the library now continues processing and returns results from modules with valid licenses. An error is still reported to indicate the license issue.
- `StartCapturing` now stops immediately and returns a license-related error code if none of the tasks have a valid license, instead of proceeding and returning an empty result.

### Fixed

- Fixed various minor bugs and improved overall stability.

## 3.0.3001(06/09/2025)

### Fixed

- Fixed an issue where the results from the last unprocessed frame were still rendered on the page after calling the `captureVisionRouter.stopCapturing()` method.

## 3.0.3000(06/05/2025)

### [Highlights](https://www.dynamsoft.com/release-highlights/?product=dcv3.0)

#### Workflow Improvements

- Restructured the parameter control hierarchy at all levels for finer scope definition and more granular process management, with the stage level newly added.
- Enabled custom combinations and sequences of sections, increasing flexibility and operational customization under specific conditions.
- Redesigned document normalization sections to better accommodate diverse document processing operations.
  
#### Deep Learning Integration

- Improved the reading rate of 1D barcode by introducing a new deblurring deep-learning model.
- Enhanced text recognition capabilities with deep learning-based text-line recognition.

#### Algorithm Enhancements

- Enabled deduplication at the Region of Interest (ROI) level to consolidate results from multiple tasks.
- Enhanced the text recognition workflow by integrating improved multi-step recognition processes and validation methods.
- Improved the `CODE_128` and `DataMatrix` DeepAnalysis algorithms for better decoding accuracy and performance.
- Added support for new barcode types: `CODE_32`, `MATRIX_25`, `KIX`, and `TELEPEN`.
- Added GS1 Application Identifiers (AI) support for improved code parsing capabilities.

#### Engineering Optimizations

- Simplified the loading and configuration of WASM resources, reducing the overall size of the WASM files.
- Added the `dcvData` package to host all potentially used resource files (such as machine learning models, code parser resources, preset template files, etc.).
- Implemented conversion functionality between `ImageData` and image files, including both local and in-memory files.
- Added utility functions for basic image processing tasks.