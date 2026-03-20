---
layout: default-layout
title: class ImageProcessor - Dynamsoft Utility Module JS Edition API Reference
description: This page shows the JS edition of the class ImageProcessor in Dynamsoft Utility Module.
keywords: image manager, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ImageProcessor

The `ImageProcessor` class provides APIs for processing images.

| Name                                              | Description                                                                        |
| ------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `static` [cropImage()](#cropimage)                         |  Crops an image using a rectangle.                                |
| `static` [cropAndDeskewImage()](#cropanddeskewimage)       |  Crops and deskew an image using a quadrilateral.                                |
| `static` [adjustBrightness()](#adjustbrightness)           |  Adjusts the brightness of the image.                                              |
| `static` [adjustContrast()](#adjustcontrast)               |  Adjusts the contrast of the image.                                                |
| `static` [filterImage()](#filterimage)                     |  Applies a specified image filter to an input image.                               |
| `static` [convertToGray()](#converttogray)                 |  Converts a colour image to grayscale.                                             |
| `static` [convertToBinaryGlobal()](#converttobinaryglobal) |  Converts a grayscale image to a binary image using a global threshold.            |
| `static` [convertToBinaryLocal()](#converttobinarylocal)   |  Converts a grayscale image to a binary image using local (adaptive) binarization. |

## cropImage

Crops an image using a rectangle.

```typescript
cropImage(image: Blob | DSImageData, roi: DSRect): Promise<DSImageData>;
```

**Parameters**

`image`: The image to be saved, of type `Blob`.

`roi`: The rectangle to be cropped.

**Return Value**

A promise that resolves with the cropped image data.

## cropAndDeskewImage

Crops and deskews an image using a quadrilateral.

```typescript
cropAndDeskewImage(image: Blob | DSImageData, roi: Quadrilateral, dstWidth: number = 0, dstHeight: number = 0, padding: number = 0): Promise<DSImageData>;
```

**Parameters**

`image`: The image to be saved, of type `Blob`.

`roi`: The quadrilateral defining the region of interest to be cropped and deskewed.

`dstWidth`: The desired width of the output image. If set to 0, the width and height will be automatically calculated.

`dstHeight`: The desired height of the output image. If set to 0, the width and height will be automatically calculated.

`padding`: Extra padding pixels applied to expand the boundaries of the extracted region.

**Return Value**

A promise that resolves with the cropped and deskewed image data.

## adjustBrightness

Adjusts the brightness of the image.

```typescript
adjustBrightness(image: Blob | DSImageData, brightness: number): Promise<DSImageData>;
```

**Parameters**

`image`: The image to be adjusted.

`brightness`: Brightness adjustment value (range: [-100, 100]).

**Return Value**

A promise that resolves with the adjusted image data.

## adjustContrast

Adjusts the contrast of the image.

```typescript
adjustContrast(image: Blob | DSImageData, contrast: number): Promise<DSImageData>;
```

**Parameters**

`image`: The image to be adjusted.

`contrast`: Contrast adjustment value (range: [-100, 100]).

**Return Value**

A promise that resolves with the adjusted image data.

## filterImage

Applies a specified image filter to an input image.

```typescript
filterImage(image: Blob | DSImageData, filterType: EnumFilterType): Promise<DSImageData>;
```

**Parameters**

`image`: The image to be filtered.

`filterType`: The type of filter to apply.

**Return Value**

A promise that resolves with the filtered image data.

## convertToGray

Converts a colour image to grayscale.

```typescript
convertToGray(image: Blob | DSImageData, R?: number, G?: number, B?: number): Promise<DSImageData>;
```

**Parameters**

`image`: The image to be converted.

`R`: [R=0.3] - Weight for the red channel.

`G`: [G=0.59] - Weight for the green channel.

`B`: [B=0.11] - Weight for the blue channel.

**Return Value**

A promise that resolves with the grayscale image data.

## convertToBinaryGlobal

Converts an image to a binary image using a global threshold.

```typescript
convertToBinaryGlobal(image: Blob | DSImageData, threshold?: number, invert?: boolean): Promise<DSImageData>;
```

**Parameters**

`image`: The grayscale image.

`threshold`: [threshold=-1] Global threshold for binarization (-1 for automatic calculation).

`invert`: [invert=false] Whether to invert the binary image.

**Return Value**

A promise that resolves with the binary image data.

## convertToBinaryLocal

Converts an image to a binary image using local (adaptive) binarization.

```typescript
convertToBinaryLocal(image: Blob | DSImageData, blockSize?: number, compensation?: number, invert?: boolean): Promise<DSImageData>;
```

**Parameters**

`image`: The grayscale image.

`blockSize`: [blockSize=0] Size of the block for local binarization.

`compensation`: [compensation=10] Adjustment value to modify the threshold.

`invert`: [invert=false] Whether to invert the binary image.

**Return Value**

A promise that resolves with the binary image data.

**Remarks**

Updated default compensation value from0 to 10 in CaptureVisionBundle version 3.4.2000 & BarcodeReaderBundle version 11.4.2000.