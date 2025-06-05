---
layout: default-layout
title: class ImageDrawer - Dynamsoft Utility Module JS Edition API Reference
description: This page shows the JS edition of the class ImageDrawer in Dynamsoft Utility Module.
keywords: image manager, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ImageDrawer

The `ImageDrawer` class provides APIs for drawing shapes on images.

| Name                          | Description                                                    |
| ----------------------------  | -------------------------------------------------------------- |
| [drawOnImage()](#drawonimage) | Draws various shapes on an image, and save it in PNG format.   |

## drawOnImage

This method draws various shapes on an image, and save it in PNG format.

```typescript
class ImageDrawer {
    /**
     * This method draws various shapes on an image, and save it in PNG format.
     *
     * @param image The image to be saved.
     * @param drawingItem An array of different shapes to draw on the image.
     * @param type The type of drawing shapes.
     * @param color The color to use for drawing. Defaults to 0xFFFF0000 (red).
     * @param thickness The thickness of the lines to draw. Defaults to 1.
     * @param download An optional boolean flag that, when set to true, triggers the download of the file.
     *
     * @returns A promise that resolves with the saved File object.
     */
    drawOnImage(
        image: Blob | string | DSImageData, 
        drawingItem: Array<Quadrilateral> | Quadrilateral | Array<LineSegment> | LineSegment | Array<Contour> | Contour | Array<Corner> | Corner | Array<Edge> | Edge, 
        type: "quads" | "lines" | "contours" | "corners" | "edges", 
        color?: number, 
        thickness?: number, 
        download?: boolean): Promise<DSImageData>;
}
```

**Parameters**

`image`: The image to be saved, of type `Blob`, `DSImageData` or `string`.

`drawingItem`: A shape or an array of different shapes to draw on the image.

`type`: The type of drawing shapes.

`color`: The color to use for drawing. Defaults to 0xFFFF0000 (red).

`thickness`: The thickness of the lines to draw. Defaults to 1.

`download`: An optional boolean flag that, when set to true, triggers the download of the file.

**Return Value**

A promise that resolves with the saved File object.