---
layout: default-layout
title: Interface LineSegmentsUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interfaace LineSegmentsUnit in Dynamsoft Core Module.
keywords: line segments, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# LineSegmentsUnit

The `LineSegmentsUnit` interface extends the `IntermediateResultUnit` interface and represents a unit of intermediate result specifically for line segments.

```typescript
interface LineSegmentsUnit extends IntermediateResultUnit {
    lineSegments: Array<LineSegment>;
}
```

## lineSegments

An array of `LineSegment` objects, each representing a segment of a line detected within the image.
