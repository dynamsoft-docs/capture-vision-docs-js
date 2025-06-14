---
layout: default-layout
title: API Reference Index - Core Module JavaScript Edition
description: This is the index page of the Core Module API Reference
keywords: Core, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Core Module
---

# DynamsoftCore Module

The Core module is defined in the namespace `Dynamsoft.Core`. It consists of the classes `CoreModule` and `ImageSourceAdapter` plus a few interfaces and enumerations.

## CoreModule Class

This class defines common functionality in the Core module.

| Name                                                                       | Description                                                                                       |
| -------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `static` [detectEnvironment()](./core-module-class.md#detectenvironment)   | Detects and returns information about the current runtime environment.                            |
| `static` [engineResourcePaths](./core-module-class.md#engineresourcepaths) | Configures the paths where the .wasm files and other necessary resources for modules are located. |
| `static` [getVersion()](./core-module-class.md#getversion)                 | Returns the version of the Core module.                                                           |
| `static` [isModuleLoaded()](./core-module-class.md#ismoduleloaded)         | Returns whether the WebAssembly (.wasm) file for the specified module is successfully loaded.     |
| `static` [loadWasm()](./core-module-class.md#loadwasm)                     | Initiates the loading process for the .wasm file(s) corresponding to the specified module(s).     |

## ImageSourceAdapter Class

The `ImageSourceAdapter` class defines how an image source should be defined in order to interact with the `CaptureVisionRouter` class. Note that this is an abstract class and can't be directly instantiated.

The APIs for this class are:

| Name                                                                                           | Description                                                                                             |
| ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| [addImageToBuffer()](./image-source-adapter.md#addimagetobuffer)                               | Adds an image to the internal buffer.                                                                   |
| [clearBuffer()](./image-source-adapter.md#clearbuffer)                                         | Clears all images from the buffer, resetting the state for new image fetching.                          |
| [getBufferOverflowProtectionMode()](./image-source-adapter.md#getbufferoverflowprotectionmode) | Returns the current mode for handling buffer overflow situations.                                       |
| [getColourChannelUsageType()](./image-source-adapter.md#getcolourchannelusagetype)             | Retrieves the current usage type for color channels in images.                                          |
| [getImage()](./image-source-adapter.md#getimage)                                               | Returns a buffered image.                                                                               |
| [getImageCount()](./image-source-adapter.md#getimagecount)                                     | Retrieves the current number of images in the buffer.                                                   |
| [getMaxImageCount()](./image-source-adapter.md#getmaximagecount)                               | Returns the maximum number of images that can be buffered at any time.                                  |
| [hasImage()](./image-source-adapter.md#hasimage)                                               | Checks if an image with the specified ID is present in the buffer.                                      |
| [hasNextImageToFetch()](./image-source-adapter.md#hasnextimagetofetch)                         | Determines whether there are more images available to fetch.                                            |
| [isBufferEmpty()](./image-source-adapter.md#isbufferempty)                                     | Determines whether the buffer is currently empty.                                                       |
| [setErrorListener()](./image-source-adapter.md#seterrorlistener)                               | Sets an error listener to receive notifications about errors that occur during image source operations. |
| [setBufferOverflowProtectionMode()](./image-source-adapter.md#setbufferoverflowprotectionmode) | Sets the behavior for handling new incoming images when the buffer is full.                             |
| [setColourChannelUsageType()](./image-source-adapter.md#setcolourchannelusagetype)             | Sets the usage type for color channels in images.                                                       |
| [setMaxImageCount()](./image-source-adapter.md#setmaximagecount)                               | Sets the maximum number of images the buffer can hold.                                                  |
| [setNextImageToReturn()](./image-source-adapter.md#setnextimagetoreturn)                       | Sets the processing priority of a specific image, affecting the order in which images are returned.     |
| [startFetching()](./image-source-adapter.md#startfetching)                                     | Starts the process of fetching images.                                                                  |
| [stopFetching()](./image-source-adapter.md#stopfetching)                                       | Stops the process of fetching images.                                                                   |

## Interfaces

The following are the basic interfaces often shared by more than one module:

### Basic Shapes

* [Arc](./basic-structures/arc.md)
* [Contour](./basic-structures/contour.md)
* [Corner](./basic-structures/corner.md)
* [DSRect](./basic-structures/ds-rect.md)
* [Edge](./basic-structures/edge.md)
* [LineSegment](./basic-structures/line-segment.md)
* [Point](./basic-structures/point.md)
* [Polygon](./basic-structures/polygon.md)
* [Quadrilateral](./basic-structures/quadrilateral.md)
* [Rect](./basic-structures/rect.md)

### Basic Structures

<!--* [CapturedResult](./basic-structures/captured-result.md)-->
* [CapturedResultBase](./basic-structures/captured-result-base.md)
* [CapturedResultItem](./basic-structures/captured-result-item.md)
* [DSFile](./basic-structures/ds-file.md)
* [DSImageData](./basic-structures/ds-image-data.md)
* [ImageSourceErrorListener](./basic-structures/image-source-error-listener.md)
* [ImageTag](./basic-structures/image-tag.md)
* [OriginalImageResultItem](./basic-structures/original-image-result-item.md)
* [TextZone](./intermediate-results/text-zone.md)
* [Warning](./basic-structures/warning.md)

<!--* [FileImageTag](./basic-structures/file-image-tag.md)-->
<!--* [PDFReadingParameter](./basic-structures/pdf-reading-parameter.md) -->

### Intermediate Results

* [BinaryImageUnit](./intermediate-results/binary-image-unit.md)
* [ColourImageUnit](./intermediate-results/colour-image-unit.md)
* [ContoursUnit](./intermediate-results/contours-unit.md)
* [EnhancedGrayscaleImageUnit](./intermediate-results/enhanced-grayscale-image-unit.md)
* [GrayscaleImageUnit](./intermediate-results/grayscale-image-unit.md)
* [IntermediateResult](./intermediate-results/intermediate-result.md)
* [IntermediateResultExtraInfo](./intermediate-results/intermediate-result-extra-info.md)
* [IntermediateResultUnit](./intermediate-results/intermediate-result-unit.md)
* [ObservationParameters](./intermediate-results/observation-parameters.md)
* [LineSegmentsUnit](./intermediate-results/line-segments-unit.md)
* [PredetectedRegionElement](./intermediate-results/predetected-region-element.md)
* [PredetectedRegionsUnit](./intermediate-results/predetected-regions-unit.md)
* [RegionObjectElement](./intermediate-results/region-object-element.md)
* [ScaledColourImageUnit](./intermediate-results/scaled-colour-image-unit.md)
* [TextRemovedBinaryImageUnit](./intermediate-results/text-removed-binary-image-unit.md)
* [TextureDetectionResultUnit](./intermediate-results/texture-detection-result-unit.md)
* [TextureRemovedBinaryImageUnit](./intermediate-results/texture-removed-binary-image-unit.md)
* [TextureRemovedGrayscaleImageUnit](./intermediate-results/texture-removed-grayscale-image-unit.md)
* [TextZonesUnit](./intermediate-results/text-zones-unit.md)
* [TransformedGrayscaleImageUnit](./intermediate-results/transformed-grayscale-image-unit.md)

## Enums

The following are the basic enumerations often shared by more than one module:

* [EnumBufferOverflowProtectionMode](./enum-buffer-overflow-protection-mode.md)
* [EnumCapturedResultItemType](./enum-captured-result-item-type.md)
* [EnumColourChannelUsageType](./enum-colour-channel-usage-type.md)
* [EnumCornerType](./enum-corner-type.md)
* [EnumCrossVerificationStatus](./enum-cross-verification-status.md)
* [EnumErrorCode](./enum-error-code.md)
* [EnumGrayscaleEnhancementMode](./enum-grayscale-enhancement-mode.md)
* [EnumGrayscaleTransformationMode](./enum-grayscale-transformation-mode.md)
* [EnumImageFileFormat](./enum-image-file-format.md)
* [EnumImagePixelFormat](./enum-image-pixel-format.md)
* [EnumImageTagType](./enum-image-tag-type.md)
* [EnumIntermediateResultUnitType](./enum-intermediate-result-unit-type.md)
* [EnumModuleName](./enum-module-name.md)
* [EnumRegionObjectElementType](./enum-region-object-element-type.md)
* [EnumSectionType](./enum-section-type.md)

<!-- * [EnumTransformMatrixType](./enum-transform-matrix-type.md) -->
<!-- * [EnumPDFReadingMode](./enum-pdf-reading-mode.md) -->
<!-- * [EnumRasterDataSource](./enum-raster-data-source.md) -->
<!-- * [EnumImageCaptureDistanceMode](./enum-image-capture-distance-mode.md)-->