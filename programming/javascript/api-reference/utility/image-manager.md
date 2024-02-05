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

The `ImageManager` class provides APIs for managing images. At present, it has only one API to save an image as a file.

| Name                        | Description                                            |
| --------------------------- | ------------------------------------------------------ |
| [saveToFile()](#savetofile) | Saves the specified image in either PNG or JPG format. |

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

A Promise that resolves to the saved File object.
