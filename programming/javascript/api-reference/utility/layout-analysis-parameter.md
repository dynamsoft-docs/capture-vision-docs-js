---
layout: default-layout
title: Interface LayoutAnalysisParameter - Dynamsoft Utility Module JS Edition API Reference
description: This page shows the JS edition of the interface LayoutAnalysisParameter in Dynamsoft Utility Module.
keywords: layout analysis parameter, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# LayoutAnalysisParameter

The `LayoutAnalysisParameter` interface provides parameters to constrain the layout analysis.

```typescript
interface LayoutAnalysisParameter {
    pattern: EnumLayoutPattern;
    axes: [LayoutAxis, LayoutAxis];
    inputImageWidth: number;
    inputImageHeight: number;
}
```

## pattern

Desired layout pattern. `LP_UNKNOWN` means auto-detect.

## axes

Configuration for the primary (axis 0) and secondary (axis 1) axes, of type [`LayoutAxis`](./layout-axis.md).

## inputImageWidth

Width of the source image in pixels. `0` means no boundary check.

## inputImageHeight

Height of the source image in pixels. `0` means no boundary check.

**Remarks**

New added in CaptureVisionBundle version 3.6.2000 & BarcodeReaderBundle version 11.6.2000.