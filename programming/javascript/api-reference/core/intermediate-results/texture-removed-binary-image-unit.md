---
layout: default-layout
title: interface TextureRemovedBinaryImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface TextureRemovedBinaryImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# TextureRemovedBinaryImageUnit

The `TextureRemovedBinaryImageUnit` interface represents a binary image unit after removing texture.

## Definition

```typescript
interface TextureRemovedBinaryImageUnit extends IntermediateResultUnit {
    imageData: Core.BasicStructures.DSImageData;
} 
```

| Properties               | Type |
|----------------------|-------------|
| [imageData](#imagedata) | *Core.BasicStructures.DSImageData* |

### imageData

The texture-removed binary image data stored in the unit.

```typescript
imageData: Core.BasicStructures.DSImageData;
```