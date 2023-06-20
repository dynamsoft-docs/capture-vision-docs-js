---
layout: default-layout
title: class CTextureRemovedGrayscaleImageUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CTextureRemovedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: text removed grayscale image, c++
needAutoGenerateSidebar: true
---

# CTextureRemovedGrayscaleImageUnit

The CTextureRemovedGrayscaleImageUnit class represents an intermediate result unit that contains grayscale image data with textures removed.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CTextureRemovedGrayscaleImageUnit : public CIntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the grayscale image data with textures removed.|

### GetImageData

Gets the grayscale image data with textures removed.

```cpp
virtual const CImageData* GetImageData() const
```

**Return value**

Returns a constant pointer to the grayscale image data with textures removed. You don't need to release the memory pointed to by the returned pointer.
