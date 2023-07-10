---
layout: default-layout
title: interface EnhancedGrayscaleImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface EnhancedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# EnhancedGrayscaleImageUnit

The EnhancedGrayscaleImageUnit interface represents a unit that contains an enhanced grayscale image as part of intermediate results.

## Definition

```ts
export interface EnhancedGrayscaleImageUnit extends IntermediateResultUnit {
                imageData: Core.BasicStructures.DSImageData;
            }
```

## Attributes Summary

| Attribute               | Type |
|----------------------|-------------|
| [`imageData`](#imageData) | *Core.BasicStructures.DSImageData* |

### imageData

The data of the enhanced grayscale image stored in the unit.

```ts
imageData: Core.BasicStructures.DSImageData;
```