---
layout: default-layout
title: Interface PDFReadingParameter - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface PDFReadingParameter in Dynamsoft Core Module.
keywords: pdf reading parameter, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# PDFReadingParameter

The `PDFReadingParameter` interface defines the structure of an object that is used to configure the PDF reading process.

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
| [mode](#mode) | *EnumPDFReadingMode* |
| [dpi](#dpi) | *number* |
| [rasterDataSource](#rasterdatasource) | *EnumRasterDataSource* |

### mode

The mode of PDF reading.

```typescript
mode: EnumPDFReadingMode;
```

### dpi

The DPI (dots per inch) value.

```typescript
dpi: number;
```

### rasterDataSource

The rasterDataSource.

```typescript
rasterDataSource: EnumRasterDataSource;
```