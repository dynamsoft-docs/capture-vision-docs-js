---
layout: default-layout
title: Interface LayoutAnalysisResult - Dynamsoft Utility Module JS Edition API Reference
description: This page shows the JS edition of the interface LayoutAnalysisResult in Dynamsoft Utility Module.
keywords: layout analysis result, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# LayoutAnalysisResult

The `LayoutAnalysisResult` interface represents the comprehensive results of the layout analysis.

```typescript
interface LayoutAnalysisResult {
    inferredQuads: Array<Quadrilateral>;
    rowCount: number;
    colCount: number;
    elements: Array<Array<LayoutElement>>;
    detectedPattern: EnumLayoutPattern;
    errorInfo: ErrorInfo;
}
```

## inferredQuads

An array of newly generated quadrilaterals.

## rowCount

The number of rows in the logical grid.

## colCount

The maximum number of columns across all rows.

## elements

A 2D layout grid. In line mode, shorter rows can be padded with `LES_NONE` elements, of type [`LayoutElement`](./layout-element.md).

## detectedPattern

The actual layout pattern detected by the engine.

## errorInfo

Error information. `errorCode` indicates the execution result and `errorString` provides a human-readable description. For successful execution, `errorCode` should be `0` and `errorString` may be empty.

**Remarks**

New added in CaptureVisionBundle version 3.6.2000 & BarcodeReaderBundle version 11.6.2000.