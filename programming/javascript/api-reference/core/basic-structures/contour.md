---
layout: default-layout
title: Interface Contour - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface Contour in Dynamsoft Core Module.
keywords: contour, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Contour

The `Contour` interface represents a contour made up of multiple points.

```typescript
interface Contour {
    points: Array<Point>;
}
```

## points

An array of [`Point`](./point.md) objects defining the vertices of the contour.
