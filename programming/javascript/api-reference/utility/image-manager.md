---
layout: default-layout
title: class ImageManager - Dynamsoft Utility Module JS Edition API Reference
description: This page shows the JS edition of the class ImageManager in Dynamsoft Utility Module.
keywords: image manager, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ImageManager

The `ImageManager` class provides APIs for managing images.

| Name                        | Description                                                    |
| --------------------------- | -------------------------------------------------------------- |
| [saveToFile()](#savetofile) | Saves the specified image in either PNG or JPG format.         |
| [drawOnImage()](#drawonimage) | Draws various shapes on an image, and save it in PNG format. |

### saveToFile

This method saves an image in either PNG or JPG format. The desired file format is inferred from the file extension provided in the 'name' parameter.

> Should the specified file format be omitted or unsupported, the data will default to being exported in PNG format.

```typescript
saveToFile(image: Core.DSImageData, name: string, download?: boolean): Promise<File>;
```

**Parameters**

`image`: The image to be saved, of type Core.DSImageData.

`name`: The name of the file, as a string, under which the image will be saved.

`download`: An optional boolean flag that, when set to true, triggers the download of the file.

**Return Value**

A Promise that resolves with the saved File object.

### drawOnImage

This method draws various shapes on an image, and save it in PNG format.

```typescript
drawOnimage(image: Blob | string,
             drawingItem: Array<Core.Quadrilateral> | Core.Quadrilateral | Array<Core.LineSegment> | Core.LineSegment | Array<Core.Contour> | Core.Contour | Array<Core.Corner> | Core.Corner | Array<Core.Edge> | Core.Edge, 
             type: "quads" | "lines" | "contours" | "edges",
             color: number,
             thickness: number,
             download?: boolean
            ): Promise<File>;
```

**Parameters**

`image`: The image to be saved, of type Core.DSImageData.

`drawingItem`: An array of different shapes to draw on the image.

`type`: The type of drawing shapes.

`color`: The color to use for drawing. Defaults to 0xFFFF0000 (red).

`thickness`: The thickness of the lines to draw. Defaults to 1.

`download`: An optional boolean flag that, when set to true, triggers the download of the file.

**Return Value**

A promise that resolves with the saved File object.