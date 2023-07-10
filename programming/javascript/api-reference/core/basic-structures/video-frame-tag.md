---
layout: default-layout
title: interface VideoFrameTag - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface VideoFrameTag in Dynamsoft Core Module.
keywords: video frame tag, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# VideoFrameTag

The `VideoFrameTag` interface extends the `Core.BasicStructures.ImageTag` interface and adds additional properties specific to video frames.

## Definition

```ts
export interface VideoFrameTag extends Core.BasicStructures.ImageTag {
            isCropped: boolean;
            cropRegion: Core.BasicStructures.DSRect;
            originalWidth: number; 
            originalHeight: number; 
            currentWidth: number; 
            currentHeight: number;
            timeSpent: number; 
            timeStamp: number; 
        }
```

## Attributes Summary

| Attribute               | Description |
|----------------------|-------------|
| [`isCropped`](#iscropped) | Determines whether the video frame is cropped. |
| [`cropRegion`](#cropRegion) | Gets the crop region of the video frame. |
| [`originalWidth`](#originalWidth) | Gets the original width of the video frame. |
| [`originalHeight`](#originalHeight) | Gets the original height of the video frame. |
| [`currentWidth`](#currentWidth) | Gets the current width of the video frame. |
| [`currentHeight`](#currentHeight) | Gets the current height of the video frame. |
| [`timeSpent`](#timeSpent) | The time spent on processing the video frame. |
| [`timeStamp`](#timeStamp) | The time stamp of the video frame.  |

### isCropped

Determines whether the video frame is cropped.

```ts
isCropped: boolean;
```

### cropRegion

A Core.BasicStructures.DSRect object representing the crop region of the video frame.

```ts
cropRegion: Core.BasicStructures.DSRect;
```

### originalWidth

Gets the original width of the video frame.

```ts
originalWidth: number;
```

### originalHeight

Gets the original height of the video frame.

```ts
originalHeight: number;
```

### currentWidth

The current width of the video frame after cropping.

```ts
currentWidth: number;
```

### currentHeight

The current height of the video frame after cropping.

```ts
currentHeight: number;
```

### timeSpent

The time spent on processing the video frame.

```ts
timeSpent: number;
```

### timeStamp

The time stamp of the video frame.

```ts
timeStamp: number;
```