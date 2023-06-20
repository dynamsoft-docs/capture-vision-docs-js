---
layout: default-layout
title: class CRawImageResultItem - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CRawImageResultItem in Dynamsoft Capture Vision Router Module.
keywords: raw image, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ CRawImageResultItem Class
permalink: /programming/cplusplus/api-reference/core/basic-structures/raw-image-result-item.html
---

# CRawImageResultItem

The `CRawImageResultItem` class represents a captured raw image result item. It is a derived class of `CCapturedResultItem` and provides an interface to get the image data.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore.dll

```cpp
class CRawImageResultItem ： public CCapturedResultItem
```

## Methods Summary

| Method                          | Description                                      |
| ------------------------------- | ------------------------------------------------ |
| [`GetImageData`](#getimagedata) | Gets the image data for the CRawImageResultItem. |

### GetImageData

Gets the image data for the CRawImageResultItem.

```cpp
virtual const CImageData* GetImageData() const = 0;
```

**Return value**

Returns a const pointer to the CImageData object that contains the image data for the CRawImageResultItem.
