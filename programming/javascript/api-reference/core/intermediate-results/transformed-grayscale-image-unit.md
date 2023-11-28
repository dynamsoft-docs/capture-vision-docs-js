---
layout: default-layout
title: interface TransformedGrayscaleImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface TransformedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# TransformedGrayscaleImageUnit

The `TransformedGrayscaleImageUnit` interface represents a transformed grayscale image.

## Definition

```typescript
interface TransformedGrayscaleImageUnit extends IntermediateResultUnit {
    imageData: Core.DSImageData;
} 
```

| Properties               | Type |
|----------------------|-------------|
| [imageData](#imagedata) | *Core.DSImageData* |

### imageData

The transformed grayscale image data stored in the unit.

```typescript
imageData: Core.DSImageData;
```