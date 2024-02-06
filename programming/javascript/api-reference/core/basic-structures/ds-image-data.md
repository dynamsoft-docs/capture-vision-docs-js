---
layout: default-layout
title: Interface DSImageData - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface DSImageData in Dynamsoft Core Module.
keywords: image data, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# DSImageData

The `DSImageData` interface defines the structure of an object that represents an image.

```typescript
export interface DSImageData {
    bytes: Uint8Array;
    format: Core.EnumImagePixelFormat;
    height: number;
    imageTag?: ImageTag;
    stride: number;
    width: number;
}
```

## bytes

The raw bytes of the image, of type Uint8Array.

**See Also**

[Uint8Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array).

## format

The pixel format of the image.

**See Also**

[EnumImagePixelFormat](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/image-pixel-format.html?lang=js)

## height

The height of the image in pixels.

## imageTag

An optional tag associated with the image data.

**See Also**

[ImageTag](https://www.dynamsoft.com/capture-vision/docs/web/programming/javascript/api-reference/core/basic-structures/image-tag.html?lang=js)

## stride

The stride (or row width) of the image in bytes.

## width

The width of the image in pixels.