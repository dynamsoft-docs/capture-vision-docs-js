---
layout: default-layout
title: Interface Polygon - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface Polygon in Dynamsoft Core Module.
keywords: Polygon, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Polygon

The `Polygon` interface represents a polygon defined by multiple points.

```typescript
interface Polygon {
    points: Array<Point>;
}
```

## points

An array of [`Point`](./point.md) objects defining the vertices of the polygon.
