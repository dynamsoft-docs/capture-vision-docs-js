---
layout: default-layout
title: API Reference Index - Capture Vision Router JavaScript Edition
description: This is the index page of the Capture Vision Router API Reference
keywords: CaptureVision, Capture, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: CVR JavaScript CaptureVisionRouter
permalink: /programming/javascript/api-reference/capture-vision-router/capture-vision-router.html
---

# CaptureVisionRouter Module

The "CaptureVisionRouter" module is defined in the namespace `Dynamsoft.CVR`. It consists of the main class `CaptureVisionRouter` and a few enumerations and interfaces.

## CaptureVisionRouter Class

A CaptureVisionRouter instance is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain [Final results]({{site.architecture}}output.html#final-results?lang=js) or [Intermediate Results]({{site.architecture}}output.html#intermediate-results?lang=js). The following code snippet shows its basic usage:

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

| API Name                               | Description                                               |
| -------------------------------------- | --------------------------------------------------------- |
| [capture()](single-process.md#capture) | Process an image or file to derive important information. |

### Process multiple images from an Image Source

| API Name                                                                                | Description                                                                  |
| --------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| [setInput](consecutive-process.md#setinput)                                             | Sets an image source to provide images for consecutive process.              |
| [addCaptureStateListener()](consecutive-process.md#addcapturestatelistener)             | Adds an object that listens to the state changes of the capture process.     |
| [removeCaptureStateListener()](consecutive-process.md#removecapturestatelistener)       | Removes an object which listens to the state changes of the capture process. |
| [addImageSourceStateListener](consecutive-process.md#addimagesourcestatelistener)       | Adds an object that listens to state changes of the image source.            |
| [removeImageSourceStateListener](consecutive-process.md#removeimagesourcestatelistener) | Removes an object which listens to state changes of the image source.        |
| [addResultReceiver()](consecutive-process.md#addresultreceiver)                         | Adds an object as the receiver of captured results.                          |
| [removeResultReceiver()](consecutive-process.md#removeresultreceiver)                   | Removes an object which was added as a receiver of captured results.         |
| [startCapturing()](consecutive-process.md#startcapturing)                               | Starts to process images consecutively.                                      |
| [stopCapturing()](consecutive-process.md#stopcapturing)                                 | Stops the consecutive process.                                               |


### Change Settings

| API Name                                                     | Description                                                                                                   |
| ------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- |
| [initSettings()](settings.md#initsettings)                   | Initializes settings with either a file or a string.                                                          |
| [outputSettings](settings.md#outputsettings)                 | Outputs a `CaptureVisionTemplate` specified by its name.                                                      |
| [getSimplifiedSettings()](settings.md#getsimplifiedsettings) | Returns a `SimplifiedCaptureVisionSettings` object for manipulating a specified `CaptureVisionTemplate`.      |
| [updateSettings()](settings.md#updatesettings)               | Updates a specified `CaptureVisionTemplate` with updated an updated `SimplifiedCaptureVisionSettings` object. |
| [resetSettings()](settings.md#resetsettings)                 | Resets settings to factory default.                                                                           |

### Auxiliary

| API Name                                      | Description                                                       |
| --------------------------------------------- | ----------------------------------------------------------------- |
| [getIntermediateResultManager](auxiliary.md#) | Whether to save the original image into a &lt;canvas&gt; element. |
| [getVersion](auxiliary.md#getVersion)         |                                                                   |

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