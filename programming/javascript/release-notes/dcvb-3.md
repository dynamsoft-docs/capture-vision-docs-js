---
layout: default-layout
title: DCVB Release Notes v3.x - Dynamsoft Capture Vision Bundle JavaScript Edition
description:  The release notes of DCVB v3.x - Dynamsoft Capture Vision Bundle JavaScript Edition.
keywords: release notes, capture vision, JavaScript, dcvb, 3.x
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftCaptureVisionBundle

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