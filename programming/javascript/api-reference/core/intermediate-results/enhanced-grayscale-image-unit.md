---
layout: default-layout
title: Interface EnhancedGrayscaleImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface EnhancedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# EnhancedGrayscaleImageUnit

The `EnhancedGrayscaleImageUnit` interface represents a unit that contains an enhanced grayscale image as part of intermediate results.

```typescript
interface EnhancedGrayscaleImageUnit extends IntermediateResultUnit {
    imageData: Core.DSImageData;
}
```

| Properties               | Type |
|----------------------|-------------|
| [imageData](#imagedata) | *Core.DSImageData* |

## imageData

The data of the enhanced grayscale image stored in the unit.

```typescript
imageData: Core.DSImageData;
```