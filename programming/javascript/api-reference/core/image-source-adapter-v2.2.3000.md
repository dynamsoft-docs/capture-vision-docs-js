---
layout: default-layout
title: class ImageSourceAdapter - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the class ImageSourceAdapter in Dynamsoft Core Module.
keywords: image source adapter, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ImageSourceAdapter

`ImageSourceAdapter` is an abstract class that defines the standard structure of an image source in the [Dynamsoft Capture Vision](https://www.dynamsoft.com/capture-vision/docs/core/architecture/) architecture.

| Name                                                               | Description                                                                                               |
| ----------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [addImageToBuffer()](#addimagetobuffer)                               | Adds an image to the buffer of the adapter.                                                               |
| [hasNextImageToFetch()](#hasnextimagetofetch)                         | Determines whether there are more images left to fetch.                                                   |
| [startFetching()](#startfetching)                                     | Starts fetching images.                                                                                   |
| [stopFetching()](#stopfetching)                                       | Stops fetching images.                                                                                    |
| [getImage()](#getimage)                                               | Returns a buffered image.                                                                                 |
| [setMaxImageCount()](#setmaximagecount)                               | Sets how many images are allowed to be buffered.                                                          |
| [getMaxImageCount()](#getmaximagecount)                               | Returns how many images can be buffered.                                                                  |
| [setBufferOverflowProtectionMode()](#setbufferoverflowprotectionmode) | Sets a mode that determines the action to take when there is a new incoming image and the buffer is full. |
| [getBufferOverflowProtectionMode()](#getbufferoverflowprotectionmode) | Returns the current buffer overflow protection mode.                                                      |
| [hasImage()](#hasimage)                                               | Determines whether the image is in the buffer or not.                                                     |
| [setNextImageToReturn()](#setnextimagetoreturn)                       | Sets the next image to return.                                                                            |
| [getImageCount()](#getimagecount)                                     | Returns the actual count of buffered images.                                                              |
| [isBufferEmpty()](#isbufferempty)                                     | Determines whether the buffer is empty.                                                                   |
| [clearBuffer()](#clearbuffer)                                         | Clears the image buffer.                                                                                  |
| [setColourChannelUsageType()](#setcolourchannelusagetype)             | Sets the usage type of a color channel in an image.                                                       |
| [getColourChannelUsageType()](#getcolourchannelusagetype)             | Gets the usage type of a color channel in an image.                                                       |

## addImageToBuffer

Adds an image to the buffer of the adapter.

```typescript
addImageToBuffer(image: Core.DSImageData): void;
```

**Parameters**

`image`: The image to add to the buffer.

## hasNextImageToFetch

An abstract method that needs to be implemented by the user. It checks if there is a next image to fetch.

```typescript
abstract hasNextImageToFetch(): boolean;
```

**Return value**

Returns true if there are more images left to fetch, false otherwise. 

## startFetching

Starts fetching images.

```typescript
startFetching(): void;
```

## stopFetching

Stops fetching images.

```typescript
stopFetching(): void;
```

## getImage

Retrieves a buffered image as a promise.

```typescript
getImage(): Promise<Core.DSImageData>;
```

**Return value**

Returns the image object as a promise .

## setMaxImageCount

Sets how many images are allowed to be buffered.

```typescript
setMaxImageCount(count: number): void;
```

**Parameters**

`count`: The maximum number of images that can be buffered.

## getMaxImageCount

Returns how many images can be buffered.

```typescript
getMaxImageCount(): number;
```

**Return value**

Returns the maximum number of images that can be buffered.

## setBufferOverflowProtectionMode

Sets a mode that determines the action to take when there is a new incoming image and the buffer is full.

```typescript
setBufferOverflowProtectionMode(mode: Core.EnumBufferOverflowProtectionMode): void;
```

**Parameters**

`mode`: The buffer overflow protection mode to set.

## getBufferOverflowProtectionMode

Returns the current buffer overflow protection mode.

```typescript
getBufferOverflowProtectionMode(): Core.EnumBufferOverflowProtectionMode;
```

**Return value**

Returns the current buffer overflow protection mode.

## hasImage

Determines whether the image is in the buffer or not.

```typescript
hasImage(imageId: number): boolean;
```

**Parameters**

`imageId`: The ID of the image to check.

**Return value**

Returns true if the image is in the buffer, false otherwise.

## setNextImageToReturn

Sets the next image to return.

```typescript
setNextImageToReturn(imageId: number, keepInBuffer?: boolean): void;
```

**Parameters**

`imageId`: The ID of the next image to return.

`keepInBuffer`: Whether the image should be kept in the buffer after it is returned.


## getImageCount

Returns the actual count of buffered images.

```typescript
getImageCount(): number;
```

**Return value**

Returns the actual count of buffered images.

## isBufferEmpty

Determines whether the buffer is empty.

```typescript
isBufferEmpty(): boolean;
```

**Return value**

Returns true if the buffer is empty, false otherwise.

## clearBuffer

Clear the image buffer.

```typescript
clearBuffer(): void;
```

## setColourChannelUsageType

Sets the usage type of a color channel in images.

```typescript
setColourChannelUsageType(type: Core.EnumColourChannelUsageType): void;
```

## getColourChannelUsageType

Gets the usage type of a color channel in images.

```typescript
getColourChannelUsageType(): Core.EnumColourChannelUsageType;
```

**Return value**

Returns the usage type of a color channel in images.
