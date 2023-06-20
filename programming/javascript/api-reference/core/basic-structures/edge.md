---
layout: default-layout
title: class CEdge - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CEdge in Dynamsoft Core Module.
keywords: edge, c++
needAutoGenerateSidebar: true
---

# CEdge

CEdge is a structure composed of two Corner points in an image. A Corner represents a point at which the image's brightness or color sharply changes. Therefore, a CEdge is a line segment connecting two such points that have been identified as Corners.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore.dll

```cpp
class CEdge 
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`startCorner`](#startcorner) | *CCorner* |
| [`endCorner`](#endcorner) | *CCorner* |

### startCorner

The start corner point of the edge.

```cpp
CCorner startCorner
```

### endCorner

The end corner point of the edge.

```cpp
CCorner endCorner
```
