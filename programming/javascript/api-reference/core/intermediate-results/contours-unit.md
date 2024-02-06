---
layout: default-layout
title: Interface ContoursUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface ContoursUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ContoursUnit

The `ContoursUnit` interface extends the `IntermediateResultUnit` interface and represents a unit of contours, which are collections of points that define the shape of an object in an image.

```typescript
interface ContoursUnit extends IntermediateResultUnit {
    contours: Array<Contour>;
}
```

## contours

An array of `Contour` objects, each representing a series of points that outline a shape within the image.

```typescript
contours: Array<Core.Contour>;
```
