---
layout: default-layout
title: interface Edge - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface Edge in Dynamsoft Core Module.
keywords: edge, JS
needAutoGenerateSidebar: true
---

# Edge

Edge is a structure composed of two Corner points in an image. A Corner represents a point at which the image's brightness or color sharply changes. Therefore, a Edge is a line segment connecting two such points that have been identified as Corners.

## Definition

```js
export interface Edge {
                startCorner: Corner;
                endCorner: Corner;
            }
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`startCorner`](#startcorner) | *Corner* |
| [`endCorner`](#endcorner) | *Corner* |

### startCorner

The start corner point of the edge.

```js
startCorner: Corner;
```

### endCorner

The end corner point of the edge.

```js
endCorner: Corner;
```
