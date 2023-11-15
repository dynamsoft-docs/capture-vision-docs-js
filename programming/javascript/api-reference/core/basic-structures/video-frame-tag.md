---
layout: default-layout
title: interface VideoFrameTag - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface VideoFrameTag in Dynamsoft Core Module.
keywords: video frame tag, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# VideoFrameTag

The `VideoFrameTag` interface extends the `Core.BasicStructures.ImageTag` interface and adds additional properties specific to video frames.

## Definition

```typescript
interface VideoFrameTag extends Core.BasicStructures.ImageTag {
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

| Properties               | Description |
|----------------------|-------------|
| [`isCropped`](#iscropped) | Determines whether the video frame is cropped. |
| [`cropRegion`](#cropregion) | Gets the crop region of the video frame. |
| [`originalWidth`](#originalwidth) | Gets the original width of the video frame. |
| [`originalHeight`](#originalheight) | Gets the original height of the video frame. |
| [`currentWidth`](#currentwidth) | Gets the current width of the video frame. |
| [`currentHeight`](#currentheight) | Gets the current height of the video frame. |
| [`timeSpent`](#timespent) | The time spent on processing the video frame. |
| [`timeStamp`](#timestamp) | The time stamp of the video frame.  |

### isCropped

Determines whether the video frame is cropped.

```typescript
isCropped: boolean;
```

### cropRegion

A Core.BasicStructures.DSRect object representing the crop region of the video frame.

```typescript
cropRegion: Core.BasicStructures.DSRect;
```

### originalWidth

Gets the original width of the video frame.

```typescript
originalWidth: number;
```

### originalHeight

Gets the original height of the video frame.

```typescript
originalHeight: number;
```

### currentWidth

The current width of the video frame after cropping.

```typescript
currentWidth: number;
```

### currentHeight

The current height of the video frame after cropping.

```typescript
currentHeight: number;
```

### timeSpent

The time spent on processing the video frame.

```typescript
timeSpent: number;
```

### timeStamp

The time stamp of the video frame.

```typescript
timeStamp: number;
```