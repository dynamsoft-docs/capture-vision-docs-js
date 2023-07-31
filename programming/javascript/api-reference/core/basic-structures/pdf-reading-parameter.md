---
layout: default-layout
title: interface PDFReadingParameter - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface PDFReadingParameter in Dynamsoft Core Module.
keywords: pdf reading parameter, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# PDFReadingParameter

The PDFReadingParameter interface represents the parameters for reading a PDF file. It contains the mode of PDF reading, the DPI (dots per inch) value, and the target content type.

## Definition

```typescript
interface PDFReadingParameter {
                mode: EnumPDFReadingMode;
                dpi: number;
                rasterDataSource: EnumRasterDataSource;
            } 
```


  
| Properties | Type |
|---------- | ---- |
| [`mode`](#mode) | *EnumPDFReadingMode* |
| [`dpi`](#dpi) | *number* |
| [`rasterDataSource`](#rasterdatasource) | *EnumRasterDataSource* |

### mode

The mode of PDF reading.

### dpi

The DPI (dots per inch) value.

### rasterDataSource

The rasterDataSource.
