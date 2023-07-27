---
layout: default-layout
title: interface ColourImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface ColourImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ColourImageUnit

The ColourImageUnit interface represents a colour image unit.

## Definition

```typescript
interface ColourImageUnit extends IntermediateResultUnit {
                imageData: Core.BasicStructures.DSImageData;
            }
```



| Properties               | Type |
|----------------------|-------------|
| [`imageData`](#imageData) | *Core.BasicStructures.DSImageData* |

### imageData

The colour image data stored in the unit.

```typescript
imageData: Core.BasicStructures.DSImageData;
```