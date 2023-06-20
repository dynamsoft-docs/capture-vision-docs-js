---
layout: default-layout
title: class CIntermediateResultUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CIntermediateResultUnit in Dynamsoft Core Module.
keywords: intermediate result, c++
needAutoGenerateSidebar: true
---

# CIntermediateResultUnit

The CIntermediateResultUnit class represents an intermediate result unit used in image processing. It is an abstract base class with multiple subclasses, each representing a different type of unit such as pre-detected regions, localized barcodes, decoded barcodes, localized text lines, binary image, gray image, etc.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CIntermediateResultUnit 
```


## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetHashId`](#gethashid) | Gets the hash ID of the unit.|
| [`GetSourceImageHashId`](#getsourceimagehashid) | Gets the hash ID of the source image. |
| [`GetSourceImageTag`](#getsourceimagetag) | Gets the image tag of the source image. |
| [`GetLocalToSourceImageTransformMatrix`](#getlocaltosourceimagetransformmatrix) | Gets the transformation matrix from local to source image coordinates. |
| [`SetLocalToSourceImageTransformMatrix`](#setlocaltosourceimagetransformmatrix) | Sets the transformation matrix from local to source image coordinates. |
| [`GetType`](#gettype) | Gets the type of the intermediate result unit. |
| [`Clone`](#clone) | Creates a copy of the intermediate result unit. |
| [`SetHashId`](#sethashid) | Sets the hash ID of the unit. |
| [`SetSourceImageHashId`](#setsourceimagehashid) | Sets the hash ID of the source image. |
| [`SetSourceImageTag`](#setsourceimagetag) | Sets the image tag of the source image. |
| [`Retain`](#retain) | Increases the reference count of the unit. |
| [`Release`](#release) | Decreases the reference count of the unit. |
| [`GetRotationTransformMatrix`](#getrotationtransformmatrix) | Gets the rotation transformation matrix of the original image relative to the rotated image.|
| [`SetRotationTransformMatrix`](#setrotationtransformmatrix) | Sets the rotation transformation matrix of the original image relative to the rotated image.|

### GetHashId

Gets the hash ID of the intermediate result unit.

```cpp
const char* GetHashId() const
```

**Return value**

Returns the hash ID of the unit. 

### GetSourceImageHashId

Gets the hash ID of the source image.

```cpp
const char* GetSourceImageHashId() const
```

**Return value**

Returns the hash ID of the source image.

### GetSourceImageTag

Gets the image tag of the source image.

```cpp
const CImageTag* GetSourceImageTag() const
```

**Return value**

Returns the image tag of the source image.

### GetLocalToSourceImageTransformMatrix

Gets the transformation matrix from local to source image coordinates.

```cpp
virtual void GetLocalToSourceImageTransformMatrix(double matrix[9]) const
```

**Parameters**

`[out] matrix` The transformation matrix.

### SetLocalToSourceImageTransformMatrix

Sets the transformation matrix from local to source image coordinates.

```cpp
virtual void SetLocalToSourceImageTransformMatrix(double matrix[9])
```

**Parameters**

`[in] matrix` The transformation matrix.

### GetType

Gets the type of the intermediate result unit.

```cpp
virtual IntermediateResultUnitType GetType() const = 0
```

**Return value**

Returns the type of the intermediate result unit.

### Clone

Creates a copy of the intermediate result unit.

```cpp
virtual CIntermediateResultUnit* Clone() const = 0
```

**Return value**

Returns a copy of the intermediate result unit.

### SetHashId

Sets the hash ID of the intermediate result unit.

```cpp
void SetHashId(const char* _hashId)
```

**Parameters**

`[in] _hashId` The hash ID to set.

### SetSourceImageHashId

Sets the hash ID of the source image.

```cpp
void SetSourceImageHashId(const char* _sourceImageHashId)
```

**Parameters**

`[in] _sourceImageHashId` The hash ID to set.

### SetSourceImageTag

Sets the image tag of the source image.

```cpp
void SetSourceImageTag(const CImageTag* _tag)
```

**Parameters**

`[in] _tag` The image tag to set.

### Retain

Increases the reference count of the intermediate result unit.

```cpp
virtual void Retain() = 0
```

### Release

Decreases the reference count of the intermediate result unit.

```cpp
virtual void Release() = 0
```

### GetRotationTransformMatrix

Gets the rotation transformation matrix of the original image relative to the rotated image.

```cpp
void GetRotationTransformMatrix(double matrix[9]) const;
```

**Parameters**

`[out] matrix` A double array which represents the rotation transform matrix.

### SetRotationTransformMatrix

Sets the rotation transformation matrix of the original image relative to the rotated image.

```cpp
void SetRotationTransformMatrix(double matrix[9]);
```

**Parameters**

`[in] matrix` A double array which represents the rotation transform matrix.