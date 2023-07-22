---
layout: default-layout
title: interface ImageTag - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface ImageTag in Dynamsoft Core Module.
keywords: image tag, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageTag

The interface ImageTag represents an image tag that can be attached to an image in a system. It contains information about the image, such as the image ID and the image tag type.

## Definition

```typescript
interface ImageTag {
                imageId: number;
                type: EnumImageTagType;
            }
```

## Attributes Summary

| Attribute            | Type |
|----------------------|-------------|
| [`imageId`](#imageId) | *Number* |
| [`type`](#type) | *EnumImageTagType* |

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