---
layout: default-layout
title: class CCorner - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CCorner in Dynamsoft Core Module.
keywords: corner, c++
needAutoGenerateSidebar: true
---

# CCorner

CCorner is a structure in an image consisting of two line segments and intersection point. A Corner represents a point at which the image's brightness or color sharply changes.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore.dll

```cpp
class CCorner 
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`type`](#type) | *CornerType* |
| [`intersection`](#intersection) | *CPoint* |
| [`line1`](#line1) | *CLineSegment* |
| [`line2`](#line2) | *CLineSegment* |

### type

The type of the corner.

```cpp
CornerType type
```

### intersection

The intersection point of the corner.

```cpp
CPoint intersection
```

### line1

The first line connected to the corner.

```cpp
CLineSegment line1
```

### line2

The second line connected to the corner.

```cpp
CLineSegment line2
```
