---
layout: default-layout
title: class CImageData - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CImageData in Dynamsoft Core Module.
keywords: image data, c++
needAutoGenerateSidebar: true
---

# CImageData

The CImageData class represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore.dll

```cpp
class CImageData 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`CImageData()`](#cimagedata-constructor) | Constructs an empty image data object. |
| [`CImageData(int _bytesLength, const unsigned char* _bytes, int _width, int _height, int _stride, ImagePixelFormat _format, int _orientation=0, const CImageTag* _tag = NULL)`](#cimagedata-constructor2) | Constructs an image data object with the specified parameters. |
| [`~CImageData()`](#cimagedata-destructor) | Destructs the image data object and frees the allocated memory. |
| [`GetBytes`](#getbytes) | Gets the image byte array. |
| [`GetBytesLength`](#getbyteslength) | Gets the length of the image byte array. |
| [`GetWidth`](#getwidth) | Gets the width of the image. |
| [`GetHeight`](#getheight) | Gets the height of the image. |
| [`GetStride`](#getstride) | Gets the stride of the image. |
| [`GetImagePixelFormat`](#getimagepixelformat) | Gets the pixel format of the image. |
| [`GetOrientation`](#getorientation) | Gets the orientation of the image. |
| [`GetImageTag`](#getimagetag) | Gets the tag of the image. |
| [`SetImageTag`](#setimagetag) | Sets the tag of the image. |

### CImageData Constructor

Constructs an empty image data object.

```cpp
CImageData()
```

### CImageData Constructor2

Constructs an image data object with the specified parameters.

```cpp
CImageData(int _bytesLength, const unsigned char* _bytes, int _width, int _height, int _stride, ImagePixelFormat _format, int _orientation=0, const CImageTag* _tag = NULL)
```

**Parameters**

`_bytesLength` The length of the image byte array.

`_bytes` The image byte array.

`_width` The width of the image.

`_height` The height of the image.

`_stride` The stride of the image.

`_format` The pixel format of the image.

`_orientation` The orientation of the image.

`_tag` The tag of the image.

### ~CImageData Destructor

Destructs the image data object and frees the allocated memory.

```cpp
virtual ~CImageData()
```

### GetBytes

Gets the image byte array.

```cpp
const unsigned char* GetBytes() const
```

**Return value**

Returns a pointer to the image byte array.

### GetBytesLength

Gets the length of the image byte array.

```cpp
int GetBytesLength() const
```

**Return value**

Returns the length of the image byte array.

### GetWidth

Gets the width of the image.

```cpp
int GetWidth() const
```

**Return value**

Returns the width of the image.

### GetHeight

Gets the height of the image.

```cpp
int GetHeight() const
```

**Return value**

Returns the height of the image.

### GetStride

Gets the stride of the image.

```cpp
int GetStride() const
```

**Return value**

Returns the stride of the image.

### GetImagePixelFormat

Gets the pixel format of the image.

```cpp
ImagePixelFormat GetImagePixelFormat() const
```

**Return value**

Returns the pixel format of the image.

### GetOrientation

Gets the orientation of the image.

```cpp
int GetOrientation() const
```

**Return value**

Returns the orientation of the image.

### GetImageTag

Gets the tag of the image.

```cpp
const CImageTag* GetImageTag() const
```

**Return value**

Returns a pointer to the tag of the image.

### SetImageTag

Sets the tag of the image.

```cpp
void SetImageTag(const CImageTag* _tag)
```

**Parameters**

`_tag` The tag of the image.
