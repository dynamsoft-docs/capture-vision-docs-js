---
layout: default-layout
title: class CCapturedResultArray - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CCapturedResultArray in Dynamsoft Core Module.
keywords: captured result array, c++
needAutoGenerateSidebar: true
---

# CCapturedResultArray

The CCapturedResultArray class represents an array of captured results.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore.dll

```cpp
class CCapturedResultArray 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetCount`](#getcount) | Gets the count of captured results.|
| [`GetResult`](#getresult) | Gets a specific captured result at a given index. |

### GetCount

Gets the count of captured results.

```cpp
virtual int GetCount() const
```

**Return value**

Returns the count of captured results.

### GetResult

Gets a specific captured result at a given index.

```cpp
virtual const CCapturedResult* GetResult(int index) const
```

**Parameters**

`[in] index` The index of the result to get.

**Return value**

Returns a pointer to the CCapturedResult object at the given index. You are not required to release the memory pointed to by the returned pointer.
