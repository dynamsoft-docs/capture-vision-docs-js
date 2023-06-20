---
layout: default-layout
title: class CCapturedResult - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CCapturedResult in Dynamsoft Core Module.
keywords: captured result, c++
needAutoGenerateSidebar: true
---

# CCapturedResult

The CCapturedResult class represents the result of a capture operation on an image. Internally, CaptureResult stores an array that contains multiple items, each of which may be a barcode, text line, detected quad, normalized image, raw image, parsed item, etc.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore.dll

```cpp
class CCapturedResult 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetSourceImageHashId`](#getsourceimagehashid) | Gets the hash ID of the source image.|
| [`GetSourceImageTag`](#getsourceimagetag) | Gets the tag of the source image.|
| [`GetCount`](#getcount) | Gets the number of items in the captured result.|
| [`GetItem`](#getitem) | Gets a specific item in the captured result.|
| [`HasItem`](#hasitem) | Check if the item is present in the array.|
| [`RemoveItem`](#removeitem) | Remove a specific item from the array in the captured result.|
| [`GetRotationTransformMatrix`](#getrotationtransformmatrix) | Get the rotation transformation matrix of the original image relative to the rotated image.|
| [`GetErrorCode`](#geterrorcode) | Gets the error code of the capture operation.|
| [`GetErrorString`](#geterrorstring) | Gets the error message of the capture operation.|

### GetSourceImageHashId

Gets the hash ID of the source image.

```cpp
const char* GetSourceImageHashId() const
```

**Return value**

Returns the hash ID of the source image as a null-terminated string. You are not required to release the memory pointed to by the returned pointer.

### GetSourceImageTag

Gets the tag of the source image.

```cpp
const CImageTag* GetSourceImageTag() const
```

**Return value**

Returns a pointer to the CImageTag object containing the tag of the source image. You are not required to release the memory pointed to by the returned pointer.

### GetCount

Gets the number of items in the captured result.

```cpp
int GetCount() const
```

**Return value**

Returns the number of items in the captured result.

### GetItem

Gets a specific item in the captured result.

```cpp
const CCapturedResultItem* GetItem(int index) const
```

**Parameters**

`[in] index` The index of the item to retrieve.

**Return value**

Returns a pointer to the CCapturedResultItem object at the specified index.

### HasItem

Check if the item is present in the array.

```cpp
bool HasItem(const CCapturedResultItem* item) const
```

**Parameters**

`[in] item` The specific item to check.

**Return value**

Returns a bool value indicating whether the item is present in the array or not.

### RemoveItem

Remove a specific item from the array in the captured result.

```cpp
int RemoveItem(const CCapturedResultItem* item)
```

**Parameters**

`[in] item` The specific item to remove.

**Return value**

Return value indicating whether the deletion was successful or not.

### GetRotationTransformMatrix

Get the rotation transformation matrix of the original image relative to the rotated image.

```cpp
void GetRotationTransformMatrix(double matrix[9]) const;
```

**Parameters**

`[out] matrix` A double array which represents the rotation transform matrix.

### GetErrorCode

Gets the error code of the capture operation.

```cpp
int GetErrorCode() const
```

**Return value**

Returns the error code of the capture operation.

### GetErrorString

Gets the error message of the capture operation.

```cpp
const char* GetErrorString() const
```

**Return value**

Returns the error message of the capture operation as a null-terminated string. You are not required to release the memory pointed to by the returned pointer.
