---
layout: default-layout
title: class CLineSegmentsUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CLineSegmentsUnit in Dynamsoft Core Module.
keywords: line segments, c++
needAutoGenerateSidebar: true
---

# CLineSegmentsUnit

The CLineSegmentsUnit class represents a collection of line segments in 2D space. It is a derived class of CIntermediateResultUnit.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CLineSegmentsUnit: public CIntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetCount`](#getcount) | Gets the number of line segments in the collection.|
| [`GetLineSegment`](#getlinesegment) | Gets the specified line segment from the collection. |

### GetCount

Gets the number of line segments in the collection.

```cpp
virtual int GetCount() const
```

**Return value**

Returns the number of line segments in the collection.

### GetLineSegment

Gets the specified line segment from the collection.

```cpp
virtual int GetLineSegement(int index, CLineSegment* line) const
```

**Parameters**

`[in] index` The index of the line segment to retrieve.

`[in, out] line` The CLineSegment object to store the retrieved line segment.

**Return value**

Returns 0 if the operation succeeds, or a negative value if an error occurs.

Note: The caller of this method is responsible for allocating memory for the `line` pointer.
