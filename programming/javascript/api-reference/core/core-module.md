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
<!--v3.0.20--Updated on 11/23/2023-->

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

| Name                                                                                           | Description                                                                                               |
| ---------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [addImageToBuffer()](./image-source-adapter.md#addimagetobuffer)                               | Adds an image to the buffer of the adapter.                                                               |
| [hasNextImageToFetch()](./image-source-adapter.md#hasnextimagetofetch)                         | Determines whether there are more images left to fetch.                                                   |
| [startFetching()](./image-source-adapter.md#startfetching)                                     | Starts fetching images.                                                                                   |
| [stopFetching()](./image-source-adapter.md#stopfetching)                                       | Stops fetching images.                                                                                    |
| [getImage()](./image-source-adapter.md#getimage)                                               | Returns a buffered image.                                                                                 |
| [setMaxImageCount()](./image-source-adapter.md#setmaximagecount)                               | Sets how many images are allowed to be buffered.                                                          |
| [getMaxImageCount()](./image-source-adapter.md#getmaximagecount)                               | Returns how many images can be buffered.                                                                  |
| [setBufferOverflowProtectionMode()](./image-source-adapter.md#setbufferoverflowprotectionmode) | Sets a mode that determines the action to take when there is a new incoming image and the buffer is full. |
| [getBufferOverflowProtectionMode()](./image-source-adapter.md#getbufferoverflowprotectionmode) | Returns the current buffer overflow protection mode.                                                      |
| [hasImage()](./image-source-adapter.md#hasimage)                                               | Determines whether the image is in the buffer or not.                                                     |
| [setNextImageToReturn()](./image-source-adapter.md#setnextimagetoreturn)                       | Sets the next image to return.                                                                            |
| [getImageCount()](./image-source-adapter.md#getimagecount)                                     | Returns the actual count of buffered images.                                                              |
| [isBufferEmpty()](./image-source-adapter.md#isbufferempty)                                     | Determines whether the buffer is empty.                                                                   |
| [clearBuffer()](./image-source-adapter.md#clearbuffer)                                         | Clears the image buffer.                                                                                  |
| [setColourChannelUsageType()](./image-source-adapter.md#setcolourchannelusagetype)             | Sets the usage type of a color channel in an image.                                                       |
| [getColourChannelUsageType()](./image-source-adapter.md#getcolourchannelusagetype)             | Gets the usage type of a color channel in an image.                                                       |
| [setErrorListener()](./image-source-adapter.md#seterrorlistener)                               | Sets the error listener to receive notifications should errors occur during image acquisition.            |

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

* [CapturedResult](./basic-structures/captured-result.md)
* [CapturedResultItem](./basic-structures/captured-result-item.md)
* [DSFile](./basic-structures/ds-file.md)
* [DSImageData](./basic-structures/ds-image-data.md)
* [ImageSourceErrorListener](./basic-structures/image-source-error-listener.md)
* [ImageTag](./basic-structures/image-tag.md)
* [OriginalImageResultItem](./basic-structures/original-image-result-item.md)

<!--
* [FileImageTag](./basic-structures/file-image-tag.md)
* [PDFReadingParameter](./basic-structures/pdf-reading-parameter.md) -->

### Intermediate Results

* [BinaryImageUnit](./intermediate-results/binary-image-unit.md)
* [ColourImageUnit](./intermediate-results/colour-image-unit.md)
* [ContoursUnit](./intermediate-results/contours-unit.md)
* [EnhancedGrayscaleImageUnit](./intermediate-results/enhanced-grayscale-image-unit.md)
* [GrayscaleImageUnit](./intermediate-results/grayscale-image-unit.md)
* [IntermediateResult](./intermediate-results/intermediate-result.md)
* [IntermediateResultExtraInfo](./intermediate-results/intermediate-result-extra-info.md)
* [IntermediateResultUnit](./intermediate-results/intermediate-result-unit.md)
* [LineSegmentsUnit](./intermediate-results/line-segments-unit.md)
* [PredetectedRegionElement](./intermediate-results/predetected-region-element.md)
* [PredetectedRegionsUnit](./intermediate-results/predetected-regions-unit.md)
* [RegionObjectElement](./intermediate-results/region-object-element.md)
* [ScaledDownColourImageUnit](./intermediate-results/scaled-down-colour-image-unit.md)
* [TextRemovedBinaryImageUnit](./intermediate-results/text-removed-binary-image-unit.md)
* [TextureDetectionResultUnit](./intermediate-results/texture-detection-result-unit.md)
* [TextureRemovedBinaryImageUnit](./intermediate-results/texture-removed-binary-image-unit.md)
* [TextureRemovedGrayscaleImageUnit](./intermediate-results/texture-removed-grayscale-image-unit.md)
* [TextZonesUnit](./intermediate-results/text-zones-unit.md)
* [TransformedGrayscaleImageUnit](./intermediate-results/transformed-grayscale-image-unit.md)

## Enums

The following are the basic enumerations often shared by more than one module:

* [EnumBufferOverflowProtectionMode]({{ site.enums }}core/buffer-overflow-protection-mode.html?lang=js)
* [EnumCapturedResultItemType]({{ site.enums }}core/captured-result-item-type.html?lang=js)
* [EnumColourChannelUsageType]({{ site.enums }}core/colour-channel-usage-type.html?lang=js)
* [EnumCornerType]({{ site.enums }}core/corner-type.html?lang=js)
* [EnumErrorCode]({{ site.enums }}core/error-code.html?lang=js)
* [EnumGrayscaleEnhancementMode]({{ site.enums }}core/grayscale-enhancement-mode.html?lang=js)
* [EnumGrayscaleTransformationMode]({{ site.enums }}core/grayscale-transformation-mode.html?lang=js)
* [EnumImagePixelFormat]({{ site.enums }}core/image-pixel-format.html?lang=js)
* [EnumImageTagType]({{ site.enums }}core/image-tag-type.html?lang=js)
* [EnumIntermediateResultUnitType]({{ site.enums }}core/intermediate-result-unit-type.html?lang=js)
* [EnumRegionObjectElementType]({{ site.enums }}core/region-object-element-type.html?lang=js)
* [EnumSectionType]({{ site.enums }}core/section-type.html?lang=js)
* [EnumTransformMatrixType]({{ site.enums }}core/transform-matrix-type.html?lang=js)

<!-- * [EnumPDFReadingMode]({{ site.enums }}core/pdf-reading-mode.html?lang=js) -->
<!-- * [EnumRasterDataSource]({{ site.enums }}core/raster-data-source.html?lang=js) -->
<!--* [EnumImageCaptureDistanceMode]({{ site.enums }}core/image-capture-distance-mode.html?lang=js)-->