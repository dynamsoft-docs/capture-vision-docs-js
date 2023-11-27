---
layout: default-layout
title: interface TextRemovedBinaryImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface TextRemovedBinaryImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# TextRemovedBinaryImageUnit

The `TextRemovedBinaryImageUnit` interface represents a binary image unit after removing text.

## Definition

```typescript
interface TextRemovedBinaryImageUnit extends IntermediateResultUnit {
    imageData: Core.BasicStructures.DSImageData;
} 
```

| Properties               | Type |
|----------------------|-------------|
| [imageData](#imagedata) | *Core.BasicStructures.DSImageData* |

### imageData

The text-removed binary image data stored in the unit.

```typescript
imageData: Core.BasicStructures.DSImageData;
```