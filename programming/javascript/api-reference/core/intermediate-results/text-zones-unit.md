---
layout: default-layout
title: Interface TextZonesUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface TextZonesUnit in Dynamsoft Core Module.
keywords: text zones, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# TextZonesUnit

The `TextZonesUnit` interface extends the `IntermediateResultUnit` interface and represents a unit of text zones identified during the processing of an image. This interface is used to encapsulate the locations of detected text areas within an image, providing a structured representation of where text is located.

```typescript
interface TextZonesUnit extends IntermediateResultUnit {
    textZones: Array<Quadrilateral>;
}
```

## textZones

An array of `Quadrilateral` objects, each representing the geometric boundaries of a detected text zone within the image.

**See Also**

[Quadrilateral](../basic-structures/quadrilateral.md)
