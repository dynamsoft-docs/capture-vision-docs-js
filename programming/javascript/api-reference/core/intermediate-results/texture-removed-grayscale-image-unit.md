---
layout: default-layout
title: interface TextureRemovedGrayscaleImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface TextureRemovedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextureRemovedGrayscaleImageUnit

The TextureRemovedGrayscaleImageUnit interface represents a grayscale image unit after removing texture.

## Definition

```typescript
interface TextureRemovedGrayscaleImageUnit extends IntermediateResultUnit {
                imageData: Core.BasicStructures.DSImageData;
            } 
```



| Properties               | Type |
|----------------------|-------------|
| [`imageData`](#imageData) | *Core.BasicStructures.DSImageData* |

### imageData

The texture-removed grayscale image data stored in the unit.

```typescript
imageData: Core.BasicStructures.DSImageData;
```