---
layout: default-layout
title: API Reference Index - Capture Vision Router JavaScript Edition
description: This is the index page for Capture Vision Router API Reference
keywords: CaptureVision, Capture, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: API Reference
permalink: /programming/javascript/api-reference/cvr/
---

# JavaScript API Reference

The "Capture Vision Router" module is defined in the namespace `Dynamsoft.CVR` which consists of the main class `CaptureVisionRouter` and a few enumerations and interfaces.

## CaptureVisionRouter

A CaptureVisionRouter instance is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain [Captured Results]() or [Intermediate Results](). The following code snippet shows its basic usage:

```js
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let imageSource = await Dynamsoft.DCE.CameraEnhancer.createInstance();
router.setInput(imageSource);
router.addResultReceiver({
    onCapturedResultReceived: (results)=> {
        console.log(results.items.length);
    }
});
router.startCapturing();
```

The APIs for this class include:

### Create and Destroy Instances

| API Name                                          | Description                                                            |
| ------------------------------------------------- | ---------------------------------------------------------------------- |
| [createInstance()](instantiate.md#createinstance) | Initializes a new instance of the `CaptureVisionRouter` class.         |
| [dispose()](instantiate.md#dispose)               | Releases all resources used by the `CaptureVisionRouter` object.       |
| [disposed](instantiate.md#disposed)               | Returns whether the `CaptureVisionRouter` object has been disposed of. |

### Process a Single Image or File

| API Name              | Description                                               |
| --------------------- | --------------------------------------------------------- |
| [capture()](#capture) | Process an image or file to derive important information. |

### Process multiple images from an Image Source

| API Name                                              | Description                                                           |
| ----------------------------------------------------- | --------------------------------------------------------------------- |
| [setInput](#setimagesource)                           | Sets an image source for continous scanning.                          |
| [addImageSourceStateListener](#onuniqueread)   | .    |
| [removeImageSourceStateListener](#onimageread) | This event is triggered after the library finishes scanning an image. |
| [addResultReceiver()](#startscanning)                 | Starts continuous scanning of incoming images.                        |
| [removeResultReceiver()](#stopscanning)               | Stops continuous scanning.                                            |
| [addCaptureStateListener()](#pausescanning)           | Pause continuous scanning but keep the video stream.                  |
| [removeCaptureStateListener()](#resumescanning)       | Resumes continuous scanning.                                          |
| [startCapturing()](#getscansettings)                  | Returns the current scan settings.                                    |
| [stopCapturing()](#updatescansettings)                | Changes scan settings with the object passed in.                      |

### Change Settings

| API Name                                          | Description                                                                  |
| ------------------------------------------------- | ---------------------------------------------------------------------------- |
| [initSettings()](#getruntimesettings)             | Returns the current runtime settings.                                        |
| [outputSettings](#initruntimesettingswithstring)  | Initializes the Runtime Settings with the settings in the given JSON string. |
| [getSimplifiedSettings()](#updateruntimesettings) | Updates runtime settings with a given struct or a preset template.           |
| [updateSettings()](#resetruntimesettings)         | Resets all parameters to default values.                                     |
| [resetSettings()](#outputruntimesettingstostring) | Return the current RuntimeSettings in the form of a string.                  |

### Auxiliary

| API Name                                                      | Description                                                       |
| ------------------------------------------------------------- | ----------------------------------------------------------------- |
| [getIntermediateResultManager](auxiliary.md#) | Whether to save the original image into a &lt;canvas&gt; element. |
| [getVersion](auxiliary.md#getVersion)                         |                                                                   |

## Interfaces and Enums

In order to make the code more predictable and readable, the library defines a series of supporting interfaces and enumerations:

### Interfaces

* [CapturedResultReceiver](interfaces/captured-result-receiver.md)
* [CaptureStateListener](interfaces/capture-state-listener.md)
* [ImageSourceStateListener](interfaces/image-source-state-listener.md)
* [RawImageResultItem](interfaces/raw-image-result-item.md)
* [SimplifiedCaptureVisionSettings](interfaces/simplified-capture-vision-settings.md)

### Enums

* [EnumImageSourceState](enums/image-source-state.md)
* [EnumCaptureState](enums/capture-state.md)