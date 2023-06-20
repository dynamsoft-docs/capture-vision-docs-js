---
layout: default-layout
title: class CFileImageTag - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CFileImageTag in Dynamsoft Core Module.
keywords: file image tag, c++
needAutoGenerateSidebar: true
---

# CFileImageTag

The CFileImageTag class represents an image tag that is associated with a file. It inherits from the CImageTag class and adds two attributes, a file path and a page number.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore.dll

```cpp
class CFileImageTag : public CImageTag
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetFilePath`](#getfilepath) | Gets the file path of the image tag.|
| [`GetPageNumber`](#getpagenumber) | Gets the page number of the image tag.|
| [`CFileImageTag`](#cfileimagetag-constructor) | The constructor of CContour. |
| [`~CFileImageTag`](#cfileimagetag-destructor) | The destructor of CContour. |

### GetFilePath

Gets the file path of the image tag.

```cpp
const char* GetFilePath() const
```

**Return value**

Returns the file path of the image tag.

### GetPageNumber

Gets the page number of the image tag.

```cpp
int GetPageNumber() const
```

**Return value**

Returns the page number of the image tag.

### CFileImageTag Constructor

The constructor of the CFileImageTag class.

```cpp
CFileImageTag(const char* _filePath, int _pageNumber)
```

**Parameters**

`[in] _filePath` The file path of the image tag.

`[in] _pageNumber` The page number of the image tag.

### CFileImageTag Destructor

The destructor of the CFileImageTag class. It frees the memory allocated for the file path.

```cpp
virtual ~CFileImageTag()
```
