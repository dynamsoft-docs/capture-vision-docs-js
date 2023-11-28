---
layout: default-layout
title: Interface DSImageData - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface DSImageData in Dynamsoft Core Module.
keywords: image data, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# DSImageData

The `DSImageData` interface defines the structure of an object that represents an image.

## Definition

```typescript
interface DSImageData {
    bytes: Uint8Array;
    width: number;
    height: number;
    stride: number;
    format: Core.EnumImagePixelFormat;
    orientation?: number;
    tag?: ImageTag;
} 
```

| Properties            | Type |
|----------------------|-------------|
| [bytes](#bytes) | *Uint8Array* |
| [width](#width) | *number* |
| [height](#height) | *number* |
| [stride](#stride) | *number* |
| [format](#format) | *Core.EnumImagePixelFormat* |
| [orientation](#orientation) | *number* |
| [tag](#tag) | *ImageTag* |

### bytes

Gets the image byte array.

```typescript
bytes: Uint8Array;
```

### width

Gets the width of the image.

```typescript
width: number;
```

### height

Gets the height of the image.

```typescript
height: number;
```

### stride

Gets the stride of the image.

```typescript
stride: number;
```

### format

Gets the pixel format of the image.

```typescript
format: Core.EnumImagePixelFormat;
```

### orientation

Gets the orientation of the image.

```typescript
orientation?: number;
```

### tag

Gets the tag of the image.

```typescript
tag?: ImageTag;
```