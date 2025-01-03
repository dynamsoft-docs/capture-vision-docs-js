---
layout: default-layout
title: Interface Quadrilateral - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface Quadrilateral in Dynamsoft Core Module.
keywords: quadrilateral, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Quadrilateral

The `Quadrilateral` interface represents a quadrilateral defined by four [Points](./point.md).

```typescript
interface Quadrilateral {
    points: [Point, Point, Point, Point];
    area?: number;
}
```

## points

An array of four `Point` objects defining the vertices of the quadrilateral.

## area

The area of the quadrilateral.