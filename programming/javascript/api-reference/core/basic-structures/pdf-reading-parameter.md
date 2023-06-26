---
layout: default-layout
title: interface PDFReadingParameter - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface PDFReadingParameter in Dynamsoft Core Module.
keywords: pdf reading parameter, JS
needAutoGenerateSidebar: true
---

# PDFReadingParameter

The PDFReadingParameter interface represents the parameters for reading a PDF file. It contains the mode of PDF reading, the DPI (dots per inch) value, and the tarGetstype.

## Definition

```js
export interface PDFReadingParameter {
                mode: EnumPDFReadingMode;
                dpi: number;
                type: EnumTargetType;
            } 
```

## Attributes Summary
  
| Attribute | Type |
|---------- | ---- |
| [`mode`](#mode) | *EnumPDFReadingMode* |
| [`dpi`](#dpi) | *number* |
| [`type`](#type) | *EnumTargetType* |

### mode

The mode of PDF reading.

### dpi

The DPI (dots per inch) value.

### type

The targetType.
