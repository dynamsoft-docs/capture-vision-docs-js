---
layout: default-layout
title: interface TextureDetectionResultUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface TextureDetectionResultUnit in Dynamsoft Core Module.
keywords: texture detection result, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# TextureDetectionResultUnit

The `TextureDetectionResultUnit` interface represents an intermediate result unit for texture detection.

## Definition

```typescript
interface TextureDetectionResultUnit extends IntermediateResultUnit {
    xSpacing: number;
    ySpacing: number;
}
```

| API Name               | Type |
|----------------------|-------------|
| [xSpacing](#xspacing) | number |
| [ySpacing](#yspacing) | number |

### xSpacing

The x-direction spacing of the texture stripes.

```typescript
xSpacing: number;
```

### ySpacing

The y-direction spacing of the texture stripes.

```typescript
ySpacing: number;
```
