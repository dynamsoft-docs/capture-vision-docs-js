---
layout: default-layout
title: class CContour - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CContour in Dynamsoft Core Module.
keywords: contour, c++
needAutoGenerateSidebar: true
---

# CContour

The CContour class represents a contour in 2D space. It contains an array of CPoint objects, which represent the vertices of the contour.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore.dll

```cpp
class CContour 
```

## Attributes Summary
  
| Attribute | Type |
|---------- | ---- |
| [`pointsCount`](#pointscount) | *int* |
| [`points`](#points)| *CPoint\** |

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`~CContour`](#ccontour-destructor) | The destructor of CContour. |

### pointsCount

The number of points in the contour.

```cpp
int pointsCount
```

### points

The point array of the contour. The memory will be released by CContour.

```cpp
CPoint* points
```

### ~CContour Destructor

The destructor of CContour. It releases the memory of the point array.

```cpp
~CContour()
```
