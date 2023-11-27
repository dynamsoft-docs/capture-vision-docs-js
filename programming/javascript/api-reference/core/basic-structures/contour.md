---
layout: default-layout
title: interface Contour - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface Contour in Dynamsoft Core Module.
keywords: contour, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Contour

The `Contour` interface defines the structure of a contour in 2-dimensional space. It contains an array of `Point` objects, which represent the vertices of the contour.

## Definition

```typescript
interface Contour {
    points: Array<Point>;
}
```
  
| Properties | Type |
|---------- | ---- |
| [points](#points)| *Array\<Point>* |

### points

The point array of the contour.

```typescript
points: Array<Point>;
```
