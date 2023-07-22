---
layout: default-layout
title: interface DSImageData - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface DSImageData in Dynamsoft Core Module.
keywords: image data, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSImageData

The DSImageData class represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.

## Definition

```typescript
interface DSImageData {
                bytes: Uint8Array;
                width: number;
                height: number;
                stride: number;
                format: Core.BasicStructures.EnumImagePixelFormat;
                orientation?: number;
                tag?: ImageTag;
            } 
```

## Attributes Summary

| Attribute            | Type |
|----------------------|-------------|
| [`bytes`](#bytes) | *Uint8Array* |
| [`width`](#width) | *number* |
| [`height`](#height) | *number* |
| [`stride`](#stride) | *number* |
| [`format`](#format) | *Core.BasicStructures.EnumImagePixelFormat* |
| [`orientation`](#orientation) | *number* |
| [`tag`](#tag) | *ImageTag* |

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
format: Core.BasicStructures.EnumImagePixelFormat;
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