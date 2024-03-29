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

# Core Module

The Core module is defined in the namespace `Dynamsoft.Core`. It consists of the classes `CoreModule`, `ImageSourceAdapter` and `IntermediateResultManager` plus a few interfaces and enumerations.

## CoreModule Class

This class defines common functionality in the Core module. At present, it has only one method.

| Name             | Description                             |
| --------------------- | --------------------------------------- |
| `static` getVersion() | Returns the version of the Core module. |

**Code snippet**

```javascript
const version = Dynamsoft.Core.CoreModule.getVersion();
console.log(version);
```

## ImageSourceAdapter Class

The `ImageSourceAdapter` class defines how an image source should be defined for it to interact with the `CaptureVisionRouter` class. Note that this is an abstract class and can't be directly instantiated.

The APIs for this class are:

| Name                                                                                                     | Description                                                                                               |
| ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [addImageToBuffer](./image-source-adapter.md#addimagetobuffer)                               | Adds an image to the buffer of the adapter.                                                               |
| [hasNextImageToFetch](./image-source-adapter.md#hasnextimagetofetch)                         | Determines whether there are more images left to fetch.                                                   |
| [startFetching](./image-source-adapter.md#startfetching)                                     | Starts fetching images.                                                                                   |
| [stopFetching](./image-source-adapter.md#stopfetching)                                       | Stops fetching images.                                                                                    |
| [getImage](./image-source-adapter.md#getimage)                                               | Returns a buffered image.                                                                                 |
| [setMaxImageCount](./image-source-adapter.md#setmaximagecount)                               | Sets how many images are allowed to be buffered.                                                          |
| [getMaxImageCount](./image-source-adapter.md#getmaximagecount)                               | Returns how many images can be buffered.                                                                  |
| [setBufferOverflowProtectionMode](./image-source-adapter.md#setbufferoverflowprotectionmode) | Sets a mode that determines the action to take when there is a new incoming image and the buffer is full. |
| [getBufferOverflowProtectionMode](./image-source-adapter.md#getbufferoverflowprotectionmode) | Returns the current buffer overflow protection mode.                                                      |
| [hasImage](./image-source-adapter.md#hasimage)                                               | Determines whether the image is in the buffer or not.                                                     |
| [setNextImageToReturn](./image-source-adapter.md#setnextimagetoreturn)                       | Sets the next image to return.                                                                            |
| [getImageCount](./image-source-adapter.md#getimagecount)                                     | Returns the actual count of buffered images.                                                              |
| [isBufferEmpty](./image-source-adapter.md#isbufferempty)                                     | Determines whether the buffer is empty.                                                                   |
| [clearBuffer](./image-source-adapter.md#clearbuffer)                                         | Clears the image buffer.                                                                                  |
| [setColourChannelUsageType](./image-source-adapter.md#setcolourchannelusagetype)             | Sets the usage type of a color channel in an image.                                                       |
| [getColourChannelUsageType](./image-source-adapter.md#getcolourchannelusagetype)             | Gets the usage type of a color channel in an image.                                                       |

## IntermediateResultManager Class

The `IntermediateResultManager` class defines a user can interact with the `CaptureVisionRouter` class about intermediate results.

The APIs for this class are:

| Name                                                                                          | Description                                          |
| -------------------------------------------------------------------------------------------------- | ---------------------------------------------------- |
| [addResultReceiver](./intermediate-results/intermediate-result-manager.md#addresultreceiver)       | Adds an intermediate result receiver.                |
| [removeResultReceiver](./intermediate-results/intermediate-result-manager.md#removeresultreceiver) | Removes an intermediate result receiver.             |
| [getOriginalImage](./intermediate-results/intermediate-result-manager.md#getoriginalimage)         | Gets the original image data using an image hash id. |

## Interfaces and Enums

In order to make the code more predictable and readable, the library defines a series of supporting interfaces and enumerations:

### Interfaces

The following are the basic interfaces often shared by more than one module:

* [Arc](./basic-structures/arc.md)
* [CapturedResultItem](./basic-structures/captured-result-item.md)
* [CapturedResultReceiver](./basic-structures/captured-result-receiver.md)
* [CapturedResult](./basic-structures/captured-result.md)
* [Contour](./basic-structures/contour.md)
* [Corner](./basic-structures/corner.md)
* [DSImageData](./basic-structures/ds-image-data.md)
* [DSRect](./basic-structures/ds-rect.md)
* [Edge](./basic-structures/edge.md)
* [ImageTag](./basic-structures/image-tag.md)
* [LineSegment](./basic-structures/line-segment.md)
* [Point](./basic-structures/point.md)
* [Polygon](./basic-structures/polygon.md)
* [Quadrilateral](./basic-structures/quadrilateral.md)
* [OriginalImageResultItem](./basic-structures/original-image-result-item.md)
* [Rect](./basic-structures/rect.md)
<!--

* [FileImageTag](./basic-structures/file-image-tag.md)
 * [PDFReadingParameter](./basic-structures/pdf-reading-parameter.md) -->
<!-- * [DSFile](./basic-structures/ds-file.md) -->

The following interfaces facilitate the use of intermediate result functions:

* [BinaryImageUnit](./intermediate-results/binary-image-unit.md)
* [ColourImageUnit](./intermediate-results/colour-image-unit.md)
* [ContoursUnit](./intermediate-results/contours-unit.md)
* [EnhancedGrayscaleImageUnit](./intermediate-results/enhanced-grayscale-image-unit.md)
* [GrayscaleImageUnit](./intermediate-results/grayscale-image-unit.md)
* [IntermediateResultExtraInfo](./intermediate-results/intermediate-result-extra-info.md)
* [IntermediateResultReceiver](./intermediate-results/intermediate-result-receiver.md)
* [IntermediateResultUnit](./intermediate-results/intermediate-result-unit.md)
* [IntermediateResult](./intermediate-results/intermediate-result.md)
* [LineSegmentsUnit](./intermediate-results/line-segments-unit.md)
* [ObservationParameters](./intermediate-results/observation-parameters.md)
* [PredetectedRegionElement](./intermediate-results/predetected-region-element.md)
* [PredetectedRegionsUnit](./intermediate-results/predetected-regions-unit.md)
* [RegionObjectElement](./intermediate-results/region-object-element.md)
* [ScaledDownColourImageUnit](./intermediate-results/scaled-down-colour-image-unit.md)
* [TextRemovedBinaryImageUnit](./intermediate-results/text-removed-binary-image-unit.md)
* [TextZonesUnit](./intermediate-results/text-zones-unit.md)
* [TextureDetectionResultUnit](./intermediate-results/texture-detection-result-unit.md)
* [TextureRemovedBinaryImageUnit](./intermediate-results/texture-removed-binary-image-unit.md)
* [TextureRemovedGrayscaleImageUnit](./intermediate-results/texture-removed-grayscale-image-unit.md)
* [TransformedGrayscaleImageUnit](./intermediate-results/transformed-grayscale-image-unit.md)

### Enums

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
<!-- * [EnumPDFReadingMode]({{ site.enums }}core/pdf-reading-mode.html?lang=js)
* [EnumRasterDataSource]({{ site.enums }}core/raster-data-source.html?lang=js) -->
<!--* [EnumImageCaptureDistanceMode]({{ site.enums }}core/image-capture-distance-mode.html?lang=js)-->

The following enumerations facilitate the use of intermediate result functions:

* [EnumIntermediateResultUnitType]({{ site.enums }}core/intermediate-result-unit-type.html?lang=js)
* [EnumRegionObjectElementType]({{ site.enums }}core/region-object-element-type.html?lang=js)
* [EnumSectionType]({{ site.enums }}core/section-type.html?lang=js)