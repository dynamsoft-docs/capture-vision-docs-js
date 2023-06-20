---
layout: default-layout
title: class CImageTag - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CImageTag in Dynamsoft Core Module.
keywords: image tag, c++
needAutoGenerateSidebar: true
---

# CImageTag

The CImageTag class represents an image tag that can be attached to an image in a system. It contains information about the image, such as the image ID and the image capture distance mode.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore.dll

```cpp
class CImageTag 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetType`](#gettype) | Gets the type of the image tag. |
| [`Clone`](#clone) | Creates a copy of the image tag. |
| [`GetImageId`](#getimageid) | Gets the ID of the image. |
| [`SetImageId`](#setimageid) | Sets the ID of the image. |
| [`GetImageCaptureDistanceMode`](#getimagecapturedistancemode) | Gets the capture distance mode of the image. |
| [`SetImageCaptureDistanceMode`](#setimagecapturedistancemode) | Sets the capture distance mode of the image. |

### GetType

Gets the type of the image tag.

```cpp
virtual ImageTagType GetType() const
```

**Return value**

Returns the type of the image tag.

### Clone

Creates a copy of the image tag.

```cpp
virtual CImageTag* Clone() const
```

**Return value**

Returns a pointer to a copy of the image tag.

### GetImageId

Gets the ID of the image.

```cpp
int GetImageId() const
```

**Return value**

Returns the ID of the image.

### SetImageId

Sets the ID of the image.

```cpp
void SetImageId(int imgId)
```

**Parameters**

`[in] imgId` The ID of the image.

### GetImageCaptureDistanceMode

Gets the capture distance mode of the image.

```cpp
ImageCaptureDistanceMode GetImageCaptureDistanceMode() const
```

**Return value**

Returns the capture distance mode of the image.

### SetImageCaptureDistanceMode

Sets the capture distance mode of the image.

```cpp
void SetImageCaptureDistanceMode(ImageCaptureDistanceMode mode)
```

**Parameters**

`[in] mode` The capture distance mode of the image.
