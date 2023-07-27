---
layout: default-layout
title: interface TransformedGrayscaleImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface TransformedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TransformedGrayscaleImageUnit

The TransformedGrayscaleImageUnit interface represents a transformed grayscale image.

## Definition

```typescript
interface TransformedGrayscaleImageUnit extends IntermediateResultUnit {
                imageData: Core.BasicStructures.DSImageData;
            } 
```



| Properties               | Type |
|----------------------|-------------|
| [`imageData`](#imageData) | *Core.BasicStructures.DSImageData* |

### imageData

The transformed grayscale image data stored in the unit.

```typescript
imageData: Core.BasicStructures.DSImageData;
```