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

```ts
export interface TransformedGrayscaleImageUnit extends IntermediateResultUnit {
                imageData: Core.BasicStructures.DSImageData;
            } 
```

## Attributes Summary

| Attribute               | Type |
|----------------------|-------------|
| [`imageData`](#imageData) | *Core.BasicStructures.DSImageData* |

### imageData

The transformed grayscale image data stored in the unit.

```ts
imageData: Core.BasicStructures.DSImageData;
```