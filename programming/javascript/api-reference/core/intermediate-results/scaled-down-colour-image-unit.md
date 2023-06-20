---
layout: default-layout
title: class CScaledDownColourImageUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CScaledDownColourImageUnit in Dynamsoft Core Module.
keywords: scaled down colour image, c++
needAutoGenerateSidebar: true
---

# CScaledDownColourImageUnit

The CScaledDownColourImageUnit class represents an intermediate result unit that contains scaled down color image. It is derived from the CIntermediateResultUnit class.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CScaledDownColourImageUnit : public CIntermediateResultUnit
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the image data of the unit.|

### GetImageData

Gets the image data of the unit.

```cpp
virtual const CImageData* GetImageData() const
```

**Return value**

Returns a pointer to the CImageData object that contains the image data of the unit. You are not required to release the memory pointed to by the returned pointer.
