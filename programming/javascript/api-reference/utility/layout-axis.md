---
layout: default-layout
title: Interface LayoutAxis - Dynamsoft Utility Module JS Edition API Reference
description: This page shows the JS edition of the interface LayoutAxis in Dynamsoft Utility Module.
keywords: layout axis, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# LayoutAxis

The `LayoutAxis` interface provides configuration for a single axis in layout analysis. Axis 0 is the primary axis, axis 1 is the secondary axis.

```typescript
interface LayoutAxis {
    elementCount: number;
    isStaggered: boolean;
    angle: number;
    isEqualSpacing: boolean;
    spacing: number;
    spacingUnit: EnumMeasureUnit;
}
```

## elementCount

Expected number of elements along this axis. `-1` means auto-detect.

## isStaggered

Whether the layout uses an offset / staggered pattern.

## angle

Target angle in `[0, 180]`. `-1` means auto-detect.

## isEqualSpacing

Whether equal spacing is enforced along this axis.

## spacing

Spacing between elements along this axis. `-1` means auto-detect.

## spacingUnit

Interpretation of the spacing value, of type `EnumMeasureUnit`.

**Remarks**

New added in CaptureVisionBundle version 3.6.2000 & BarcodeReaderBundle version 11.6.2000.