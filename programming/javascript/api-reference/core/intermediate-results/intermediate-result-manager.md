---
layout: default-layout
title: class CIntermediateResultManager - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CIntermediateResultManager in Dynamsoft Core Module.
keywords: intermediate result manager, c++
needAutoGenerateSidebar: true
---

# CIntermediateResultManager

The CIntermediateResultManager class manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get raw image data using an image hash id.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CIntermediateResultManager 
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`AddResultReceiver`](#addresultreceiver) | Adds an intermediate result receiver.|
| [`RemoveResultReceiver`](#removeresultreceiver) | Removes an intermediate result receiver. |
| [`GetRawImage`](#getrawimage) | Gets the raw image data using an image hash id. |

### AddResultReceiver

Adds an intermediate result receiver to the manager.

```cpp
virtual void AddResultReceiver(CIntermediateResultReceiver* receiver)
```

**Parameters**

`[in] receiver` The intermediate result receiver to add.

### RemoveResultReceiver

Removes an intermediate result receiver from the manager.

```cpp
virtual void RemoveResultReceiver(CIntermediateResultReceiver* receiver)
```

**Parameters**

`[in] receiver` The intermediate result receiver to remove.

### GetRawImage

Gets the raw image data using an image hash id.

```cpp
virtual CImageData* GetRawImage(const char* imageHashId)
```

**Parameters**

`[in] imageHashId` The hash id of the image to retrieve.

**Return value**

Returns a pointer to the CImageData object containing the raw image data. You don't need to release the memory pointed to by the returned pointer.
