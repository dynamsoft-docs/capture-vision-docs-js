---
layout: default-layout
title: class CTextRemovedBinaryImageUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CTextRemovedBinaryImageUnit in Dynamsoft Core Module.
keywords: text removed binary image, c++
needAutoGenerateSidebar: true
---

# CTextRemovedBinaryImageUnit

The CTextRemovedBinaryImageUnit class represents an intermediate result unit that contains a binary image with the text removed.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CTextRemovedBinaryImageUnit : public CIntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the binary image data with the text removed. |

### GetImageData

Gets the binary image data with the text removed.

```cpp
virtual const CImageData* GetImageData() const;
```

**Return value**

Returns a pointer to the CImageData object that contains the binary image data with the text removed. You don't need to release the memory pointed to by the returned pointer.
