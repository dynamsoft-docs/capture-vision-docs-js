---
layout: default-layout
title: interface TextureRemovedBinaryImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface TextureRemovedBinaryImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextureRemovedBinaryImageUnit

The TextureRemovedBinaryImageUnit interface represents a binary image unit after removing texture.

## Definition

```ts
export interface TextureRemovedBinaryImageUnit extends IntermediateResultUnit {
                imageData: Core.BasicStructures.DSImageData;
            } 
```

## Attributes Summary

| Attribute               | Type |
|----------------------|-------------|
| [`imageData`](#imageData) | *Core.BasicStructures.DSImageData* |

### imageData

The texture-removed binary image data stored in the unit.

```ts
imageData: Core.BasicStructures.DSImageData;
```