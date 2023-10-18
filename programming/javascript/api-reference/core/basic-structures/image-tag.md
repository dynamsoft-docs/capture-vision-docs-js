---
layout: default-layout
title: interface ImageTag - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface ImageTag in Dynamsoft Core Module.
keywords: image tag, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageTag

The `ImageTag` interface defines a structure that stores information about an image returned by an [image source](https://www.dynamsoft.com/capture-vision/docs/core/architecture/input.html).

## Definition

```typescript
interface ImageTag {
    imageId: number;
    type: EnumImageTagType;
}
```

| Properties            | Type               |
| --------------------- | ------------------ |
| [`imageId`](#imageid) | *Number*           |
| [`type`](#type)       | *EnumImageTagType* |

### imageId

The imageId attached to the image.

```typescript
imageId: number;
```

### type

The image tag type (image file or video frame) attached to the image.

```typescript
type: EnumImageTagType;
```