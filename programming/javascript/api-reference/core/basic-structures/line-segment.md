---
layout: default-layout
title: class CLineSegment - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CLineSegment in Dynamsoft Core Module.
keywords: line segment, c++
needAutoGenerateSidebar: true
---

# CLineSegment

The CLineSegment class represents a line segment in 2D space. It contains two CPoint objects, which represent the start point and end point of the line segment.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore.dll

```cpp
class CLineSegment 
```

## Attributes Summary

| Attribute | Type |
|---------- | ---- |
| [`startPoint`](#startPoint) | *CPoint* |
| [`endPoint`](#endPoint) | *CPoint* |

### startPoint

The start point of the line segment.

```cpp
CPoint startPoint
```

### endPoint

The end point of the line segment.

```cpp
CPoint endPoint
```

Here's an example of how to use the CLineSegment class:

```cpp
CLineSegment line;
line.startPoint.coordinate[0] = 0;
line.startPoint.coordinate[1] = 0;
line.endPoint.coordinate[0] = 100;
line.endPoint.coordinate[1] = 100;
```
