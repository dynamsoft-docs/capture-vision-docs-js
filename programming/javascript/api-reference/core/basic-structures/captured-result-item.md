---
layout: default-layout
title: class CCapturedResultItem - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CCapturedResultItem in Dynamsoft Core Module.
keywords: captured result item, c++
needAutoGenerateSidebar: true
---

# CCapturedResultItem

The CCapturedResultItem class represents an item in a captured result. It is an abstract base class with multiple subclasses, each representing a different type of captured item such as barcode, text line, detected quad, normalized image, raw image, parsed item, etc.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore.dll

```cpp
class CCapturedResultItem 
```

## Methods Summary

| Method                         | Description|
|--------------------------------|------------|
| [`~CCapturedResultItem`](#ccapturedresultitem-destructor) | This is the class destructor.                                                                                                |
| [`GetType`](#gettype)              | Gets the type of the captured result item.                                                                                                       |
| [`GetReferencedItem`](#getreferenceditem)    | Gets a pointer to the referenced item in the captured result.                                                                                      |

### CCapturedResultItem Destructor

This is the class destructor.

```cpp
virtual ~CCapturedResultItem(){};
```

### GetType

Gets the type of the captured result item.

```cpp
virtual CapturedResultItemType GetType() const
```

**Return value**

Returns the type of the captured result item.

### GetReferencedItem

Gets a pointer to the referenced item in the captured result item.

```cpp
virtual const CCapturedResultItem* GetReferencedItem() const
```

**Return value**

Returns a pointer to the referenced item in the captured result item. You are not required to release the memory pointed to by the returned pointer.
