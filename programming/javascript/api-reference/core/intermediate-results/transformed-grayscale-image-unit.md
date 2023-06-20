---
layout: default-layout
title: class CTransformedGrayscaleImageUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CTransformedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: transformed grayscale image, c++
needAutoGenerateSidebar: true
---

# CTransformedGrayscaleImageUnit

The CTransformedGrayscaleImageUnit class is a subclass of CIntermediateResultUnit that represents a transformed grayscale image. It may be the original grayscale image or the inverted image of the original grayscale image.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CTransformedGrayscaleImageUnit : public CIntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the image data of the transformed grayscale image.|

### GetImageData

Gets the image data of the transformed grayscale image. It may be the original grayscale image or the inverted image of the original grayscale image.

```cpp
virtual const CImageData* GetImageData() const
```

**Return value**

Returns a const pointer to a CImageData object that represents the image data of the transformed grayscale image. You don't need to release the memory pointed to by the returned pointer.
