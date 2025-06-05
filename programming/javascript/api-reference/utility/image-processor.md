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
| [cropImage()](#cropimage)                         |  Crops an image using a rectangle or quadrilateral.                                |
| [adjustBrightness()](#adjustbrightness)           |  Adjusts the brightness of the image.                                              |
| [adjustContrast()](#adjustcontrast)               |  Adjusts the contrast of the image.                                                |
| [filterImage()](#filterimage)                     |  Applies a specified image filter to an input image.                               |
| [convertToGray()](#converttogray)                 |  Converts a colour image to grayscale.                                             |
| [convertToBinaryGlobal()](#converttobinaryglobal) |  Converts a grayscale image to a binary image using a global threshold.            |
| [convertToBinaryLocal()](#converttobinarylocal)   |  Converts a grayscale image to a binary image using local (adaptive) binarization. |

## cropImage

Crops an image using a rectangle or quadrilateral.

```typescript
cropImage(image: Blob, roi: DSRect | Quadrilateral): Promise<DSImageData>;
```

**Parameters**

`image`: The image to be saved, of type `Blob`.

`roi`: The rectangle or quadrilateral to be cropped.

**Return Value**

A promise that resolves with the cropped image data.

## adjustBrightness

Adjusts the brightness of the image.

```typescript
adjustBrightness(image: Blob, brightness: number): Promise<DSImageData>;
```

**Parameters**

`image`: The image to be adjusted.

`brightness`: Brightness adjustment value (range: [-100, 100]).

**Return Value**

A promise that resolves with the adjusted image data.

## adjustContrast

Adjusts the contrast of the image.

```typescript
adjustContrast(image: Blob, contrast: number): Promise<DSImageData>;
```

**Parameters**

`image`: The image to be adjusted.

`contrast`: Contrast adjustment value (range: [-100, 100]).

**Return Value**

A promise that resolves with the adjusted image data.

## filterImage

Applies a specified image filter to an input image.

```typescript
filterImage(image: Blob, filterType: EnumFilterType): Promise<DSImageData>;
```

**Parameters**

`image`: The image to be filtered.

`filterType`: The type of filter to apply.

**Return Value**

A promise that resolves with the filtered image data.

## convertToGray

Converts a colour image to grayscale.

```typescript
convertToGray(image: Blob, R?: number, G?: number, B?: number): Promise<DSImageData>;
```

**Parameters**

`image`: The image to be converted.

`R`: [R=0.3] - Weight for the red channel.

`G`: [G=0.59] - Weight for the green channel.

`B`: [B=0.11] - Weight for the blue channel.

**Return Value**

A promise that resolves with the grayscale image data.

## convertToBinaryGlobal

Converts a grayscale image to a binary image using a global threshold.

```typescript
convertToBinaryGlobal(image: Blob, threshold?: number, invert?: boolean): Promise<DSImageData>;
```

**Parameters**

`image`: The grayscale image.

`threshold`: [threshold=-1] Global threshold for binarization (-1 for automatic calculation).

`invert`: [invert=false] Whether to invert the binary image.

**Return Value**

A promise that resolves with the binary image data.

## convertToBinaryLocal

Converts a grayscale image to a binary image using local (adaptive) binarization.

```typescript
convertToBinaryLocal(image: Blob, blockSize?: number, compensation?: number, invert?: boolean): Promise<DSImageData>;
```

**Parameters**

`image`: The grayscale image.

`blockSize`: [blockSize=0] Size of the block for local binarization.

`compensation`: [compensation=0] Adjustment value to modify the threshold.

`invert`: [invert=false] Whether to invert the binary image.

**Return Value**

A promise that resolves with the binary image data.