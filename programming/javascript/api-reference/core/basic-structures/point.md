---
layout: default-layout
title: class CPoint - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CPoint in Dynamsoft Core Module.
keywords: point, c++
needAutoGenerateSidebar: true
---

# CPoint

The CPoint class represents a point in 2D space. It contains an array of two integers, which represent the coordinates of the point.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore.dll

```cpp
class CPoint 
```

## Attributes Summary

| Attribute | Type |
|---------- | ---- |
| [`coordinate`](#coordinate) | *int[2]* |

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`TransformCoordinates`](#transformcoordinates) | Transforms the coordinates of a point using a given transformation matrix. |

### coordinate

The coordinate array of the point.

```cpp
int coordinate[2]
```

### TransformCoordinates

Transforms the coordinates of a point using a given transformation matrix.

```cpp
static CPoint TransformCoordinates(CPoint originalPoint, double transformationMatrix[9])
```

**Parameters**

`[in] originalPoint` The original point to transform.

`[in] transformationMatrix` The transformation matrix to apply to the coordinates.

**Return value**

Returns a new CPoint object with the transformed coordinates.

**Code Snippet**

```cpp
CPoint originalPoint;
originalPoint.coordinate[0] = 10;
originalPoint.coordinate[1] = 20;

double transformationMatrix[9] = {1, 0, 0, 0, 2, 0, 0, 0, 1};

CPoint transformedPoint = CPoint::TransformCoordinates(originalPoint, transformationMatrix);
```
