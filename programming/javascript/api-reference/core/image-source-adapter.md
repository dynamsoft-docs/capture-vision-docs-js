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

The `ImageSourceAdapter` class is an abstract class representing an adapter for image sources, providing a framework for fetching, buffering, and managing images from various sources. Implementations must provide specific mechanisms for image retrieval and handling.

| Name                                                                  | Description                                                                                             |
| --------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| [addImageToBuffer()](#addimagetobuffer)                               | Adds an image to the internal buffer.                                                                   |
| [clearBuffer()](#clearbuffer)                                         | Clears all images from the buffer, resetting the state for new image fetching.                          |
| [getBufferOverflowProtectionMode()](#getbufferoverflowprotectionmode) | Returns the current mode for handling buffer overflow situations.                                       |
| [getColourChannelUsageType()](#getcolourchannelusagetype)             | Retrieves the current usage type for color channels in images.                                          |
| [getImage()](#getimage)                                               | Returns a buffered image.                                                                               |
| [getImageCount()](#getimagecount)                                     | Retrieves the current number of images in the buffer.                                                   |
| [getMaxImageCount()](#getmaximagecount)                               | Returns the maximum number of images that can be buffered at any time.                                  |
| [hasImage()](#hasimage)                                               | Checks if an image with the specified ID is present in the buffer.                                      |
| [hasNextImageToFetch()](#hasnextimagetofetch)                         | Determines whether there are more images available to fetch.                                            |
| [isBufferEmpty()](#isbufferempty)                                     | Determines whether the buffer is currently empty.                                                       |
| [setErrorListener()](#seterrorlistener)                               | Sets an error listener to receive notifications about errors that occur during image source operations. |
| [setBufferOverflowProtectionMode()](#setbufferoverflowprotectionmode) | Sets the behavior for handling new incoming images when the buffer is full.                             |
| [setColourChannelUsageType()](#setcolourchannelusagetype)             | Sets the usage type for color channels in images.                                                       |
| [setMaxImageCount()](#setmaximagecount)                               | Sets the maximum number of images the buffer can hold.                                                  |
| [setNextImageToReturn()](#setnextimagetoreturn)                       | Sets the processing priority of a specific image, affecting the order in which images are returned.     |
| [startFetching()](#startfetching)                                     | Starts the process of fetching images.                                                                  |
| [stopFetching()](#stopfetching)                                       | Stops the process of fetching images.                                                                   |

## addImageToBuffer

Adds an image to the internal buffer.

```typescript
addImageToBuffer(image: DSImageData): void;
```

**Parameters**

`image`: The image to add to the buffer.

**Return value**

None.

## clearBuffer

Clears all images from the buffer, resetting the state for new image fetching.

```typescript
clearBuffer(): void;
```

**Parameters**

None.

**Return value**

None.

## getBufferOverflowProtectionMode

Returns the current mode for handling buffer overflow situations.

```typescript
getBufferOverflowProtectionMode(): EnumBufferOverflowProtectionMode;
```

**Parameters**

None.

**Return value**

The current buffer overflow protection mode.

**See Also**

[EnumBufferOverflowProtectionMode](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/buffer-overflow-protection-mode.html?lang=js)

## getColourChannelUsageType

Retrieves the current usage type for color channels in images.

```typescript
getColourChannelUsageType(): EnumColourChannelUsageType;
```

**Parameters**

None.

**Return value**

The current usage type for color channels in images.

**See Also**

[EnumColourChannelUsageType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/colour-channel-usage-type.html?lang=js)

## getImage

Returns a buffered image.

```typescript
getImage(): Promise<DSImageData>;
```

**Parameters**

None.

**Return value**

A promise that resolves with an instance of `DSImageData`.

## getImageCount

Retrieves the current number of images in the buffer.

```typescript
getImageCount(): number;
```

**Parameters**

None.

**Return value**

The actual count of buffered images.

## getMaxImageCount

Returns the maximum number of images that can be buffered at any time.

```typescript
getMaxImageCount(): number;
```

**Parameters**

None.

**Return value**

The maximum number of images that can be buffered.

## hasImage

Checks if an image with the specified ID is present in the buffer.

```typescript
hasImage(imageId: number): boolean;
```

**Parameters**

`imageId`: The ID of the image to check.

**Return value**

True if the image is in the buffer, false otherwise.

## hasNextImageToFetch

Determines whether there are more images available to fetch. This is an abstract method that needs to be implemented by the user.
   
```typescript
abstract hasNextImageToFetch(): boolean;
```

**Parameters**

None.

**Return value**

True if there are more images left to fetch, false otherwise.

## isBufferEmpty

Determines whether the buffer is currently empty.

```typescript
isBufferEmpty(): boolean;
```

**Parameters**

None.

**Return value**

True if the buffer is empty, false otherwise.

## setErrorListener

Sets an error listener to receive notifications about errors that occur during image source operations. Implementing classes should invoke the listener's onErrorReceived method with relevant error details when
```typescript
setErrorListener: (listener: ImageSourceErrorListener) => void;
```

**Parameters**

`listener`: an instance of `ImageSourceErrorListener` or its derived class to handle error notifications.

**Return value**

None.

**Code Snippet**

```javascript
cameraEnhancer.setErrorListener({
    onErrorReceived: (errorCode, errorMessage) => {
        console.log(errorMessage);
    },
});
```

**See Also**

[ImageSourceErrorListener](./basic-structures/![alt](https://))

## setBufferOverflowProtectionMode

Sets the behavior for handling new incoming images when the buffer is full.

```typescript
setBufferOverflowProtectionMode(mode: EnumBufferOverflowProtectionMode): void;
```

**Parameters**

`mode`: One of the modes defined in `EnumBufferOverflowProtectionMode`, specifying how to handle buffer overflow.

**Return value**

None.

**See Also**

[EnumBufferOverflowProtectionMode](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/buffer-overflow-protection-mode.html?lang=js)

## setColourChannelUsageType

Sets the usage type for color channels in images.

```typescript
setColourChannelUsageType(type: EnumColourChannelUsageType): void;
```

**Parameters**

`type`: one of the types defined in `EnumColourChannelUsageType`, specifying how color channels should be used.

**Return value**

None.

**See Also**

[EnumColourChannelUsageType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/colour-channel-usage-type.html?lang=js)

## setMaxImageCount

Sets the maximum number of images the buffer can hold.

```typescript
setMaxImageCount(count: number): void;
```

**Parameters**

`count`: The maximum number of images that can be buffered.

**Return value**

None.

## setNextImageToReturn

Sets the processing priority of a specific image, affecting the order in which images are returned.

```typescript
setNextImageToReturn(imageId: number, keepInBuffer?: boolean): void;
```

**Parameters**

`imageId`: The ID of the next image to return.

`keepInBuffer`: Optional. Whether the image should be kept in the buffer after it is returned.

**Return value**

None.

## startFetching

Starts the process of fetching images.

```typescript
startFetching(): void;
```

**Parameters**

None.

**Return value**

None.

## stopFetching

Stops the process of fetching images.

```typescript
stopFetching(): void;
```

**Parameters**

None.

**Return value**

None.
