---
layout: default-layout
title: class CIntermediateResult - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CIntermediateResult in Dynamsoft Core Module.
keywords: task results, intermediate results, c++
needAutoGenerateSidebar: true
---

# CIntermediateResult

The CIntermediateResult class represents a container containing a collection of CIntermediateResultUnit objects.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CIntermediateResult
```

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the number of CIntermediateResultUnit objects in the collection. |
| [`GetIntermediateResultUnit`](#getintermediateresultunit) | Gets a pointer to a specific CIntermediateResultUnit object in the collection. |

### GetCount

Gets the number of CIntermediateResultUnit objects in the collection.

```cpp
virtual int GetCount() const
```

**Return value**

Returns the number of CIntermediateResultUnit objects in the collection.

### GetIntermediateResultUnit

Gets a pointer to a specific CIntermediateResultUnit object in the collection.

```cpp
virtual const CIntermediateResultUnit* GetIntermediateResultUnit(int index) const
```

**Parameters**

`[in] index` The index of the CIntermediateResultUnit object to retrieve.

**Return value**

Returns a const pointer to the specified CIntermediateResultUnit object in the collection. You don't need to release the memory pointed to by the returned pointer.
