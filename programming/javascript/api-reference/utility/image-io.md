---
layout: default-layout
title: class ImageIO - Dynamsoft Utility Module JS Edition API Reference
description: This page shows the JS edition of the class ImageIO in Dynamsoft Utility Module.
keywords: image manager, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ImageIO

The `ImageIO` class provides APIs for images reading and saving.

| Name                                | Description                                                    |
| ----------------------------------- | -------------------------------------------------------------- |
| [saveToFile()](#savetofile)         | Saves the specified image in either PNG or JPG format.         |
| [readFromFile()](#readfromfile)     | Reads an image from a file                                     |
| [saveToMemory()](#savetomemory)     | Saves an image to memory.                                      |
| [readFromMemory()](#readfrommemory) | Reads image data from memory using the specified ID.           |

## saveToFile

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

## readFromFile

This method reads an image from a file. The file format is automatically detected based on the file extension content.

```typescript
readFromFile(file: File): Promise<DSImageData>;
```

**Parameters**

`file`: The file to read, as a `File` object.

**Return Value**

A promise that resolves with the loaded image of type `DSImageData`.

## saveToMemory

This method saves an image to memory. The desired file format is inferred from the 'format' parameter.

> Should the specified file format be omitted or unsupported, the data will default to being exported in PNG format.

```typescript
saveToMemory(image: Blob, format: Core.EnumImageFileFormat) : Promise<number>;
```

**Parameters**

`image`: A `Blob` representing the image to be saved.

`format`: The desired image format.

**Return Value**

A Promise that resolves to a memory ID which can later be used to retrieve the image via readFromMemory.

## readFromMemory

Reads image data from memory using the specified ID.

```typescript
readFromMemory(id: number) : Promise<Core.DSImageData>;
```

**Parameters**

`id`: The memory ID referencing a previously stored image.

**Return Value**

A Promise that resolves to the `DSImageData` object.