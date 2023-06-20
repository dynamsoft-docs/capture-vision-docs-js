---
layout: default-layout
title: class CBinaryImageUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CBinaryImageUnit in Dynamsoft Core Module.
keywords: binary image, c++
needAutoGenerateSidebar: true
---

# CBinaryImageUnit

The CBinaryImageUnit class represents a binary image unit that inherits from CIntermediateResultUnit. It inherits from the CIntermediateResultUnit class and stores binary image data.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CBinaryImageUnit : public CIntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets a pointer to the binary image data. |

### GetImageData

Gets a pointer to the binary image data.

```cpp
virtual const CImageData* GetImageData() const
```

**Return value**

Returns a pointer to the CBinaryImageData object containing the binary image data. You don't need to release the memory pointed to by the returned pointer.
