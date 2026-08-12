---
layout: default-layout
title: class LayoutAnalyzer - Dynamsoft Utility Module JS Edition API Reference
description: This page shows the JS edition of the class LayoutAnalyzer in Dynamsoft Utility Module.
keywords: layout analyzer, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# LayoutAnalyzer

The `LayoutAnalyzer` class provides static methods to analyze the spatial distribution of quadrilaterals.

| Name                                                    | Description                                                         |
| ------------------------------------------------------- | ------------------------------------------------------------------- |
| `static` [analyze()](#analyze)                          | Analyzes the spatial distribution of quadrilaterals.                |

## analyze

Analyzes the spatial distribution of quadrilaterals.

```typescript
static analyze(inputQuads: Array<Quadrilateral>, parameter?: LayoutAnalysisParameter): Promise<LayoutAnalysisResult>;
```

**Parameters**

`inputQuads`: An array of input quadrilaterals.

`parameter`: Optional parameters to constrain the analysis.

**Return Value**

A promise that resolves with a [`LayoutAnalysisResult`](./layout-analysis-result.md) object.

**Remarks**

New added in CaptureVisionBundle version 3.6.2000 & BarcodeReaderBundle version 11.6.2000.