---
layout: default-layout
title: class CQuadrilateral - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CQuadrilateral in Dynamsoft Core Module.
keywords: quadrilateral, c++
needAutoGenerateSidebar: true
---

# CQuadrilateral

The CQuadrilateral class represents a quadrilateral shape in 2D space. It contains an array of four CPoint objects, which represent the vertices of the quadrilateral.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore.dll

```cpp
class CQuadrilateral 
```

## Attributes Summary
  
| Attribute | Type |
|---------- | ---- |
| [`points`](#points) | *CPoint* |

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`Contains`](#contains) | Determines whether a point is inside the quadrilateral.|
| [`GetArea`](#getarea) | Gets the area of the quadrilateral. |

### points

The point array of the quadrilateral.

```cpp
CPoint points[4]
```

### Contains

Determines whether a point is inside the quadrilateral.

```cpp
bool Contains(const CPoint* point) const
```

**Parameters**

`[in] point` The point to test.

**Return value**

Returns true if the point inside the quadrilateral, false otherwise. 

### GetArea

Gets the area of the quadrilateral.

```cpp
int GetArea() const
```

**Return value**

Returns the area of the quadrilateral.
