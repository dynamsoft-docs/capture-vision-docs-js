---
layout: default-layout
title: Interface GrayscaleImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface GrayscaleImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# GrayscaleImageUnit

The `GrayscaleImageUnit` interface represents a unit that contains a grayscale image as part of intermediate results.

## Definition

```typescript
interface GrayscaleImageUnit extends IntermediateResultUnit {
    imageData: Core.DSImageData;
}
```

| Properties               | Type |
|----------------------|-------------|
| [imageData](#imagedata) | *Core.DSImageData* |

### imageData

The data of the enhanced grayscale image stored in the unit.

```typescript
imageData: Core.DSImageData;
```