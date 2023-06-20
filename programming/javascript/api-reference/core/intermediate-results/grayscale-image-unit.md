---
layout: default-layout
title: class CGrayscaleImageUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CGrayscaleImageUnit in Dynamsoft Core Module.
keywords: grayscale image, c++
needAutoGenerateSidebar: true
---

# CGrayscaleImageUnit

The CGrayscaleImageUnit class represents a grayscale image unit. It is a subclass of CIntermediateResultUnit. It is derived from the CIntermediateResultUnit class.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CGrayscaleImageUnit : public CIntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the image data of the grayscale image.|

### GetImageData

Gets the image data of the grayscale image.

```cpp
virtual const CImageData* GetImageData() const
```

**Return value**

Returns a pointer to the CImageData object that contains the grayscale image. You are not required to release the memory pointed to by the returned pointer.
