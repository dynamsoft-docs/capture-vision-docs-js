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

The `CaptureVisionRouter` class defines how a user interact with image-processing and semantic-processing products in their applications. A `CaptureVisionRouter` instance accepts an image source and returns processing results which may contain [Final results]({{site.architecture}}output.html#final-results?lang=js) or [Intermediate Results]({{site.architecture}}output.html#intermediate-results?lang=js). The following code snippet shows its basic usage:

```js
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let imageSource = await Dynamsoft.DCE.CameraEnhancer.createInstance();
router.setInput(imageSource);
router.addResultReceiver({
    onCapturedResultReceived: (results)=> {
        // Print out how many results are available.
        console.log(results.items.length);
    }
});
router.startCapturing();
```

The APIs for this class include:

### Create and Destroy Instances

| API Name                                          | Description                                                            |
| ------------------------------------------------- | ---------------------------------------------------------------------- |
| [createInstance()](./instantiate.md#createinstance) | Initializes a new instance of the `CaptureVisionRouter` class.         |
| [dispose()](./instantiate.md#dispose)               | Releases all resources used by the `CaptureVisionRouter` object.       |
| [disposed](./instantiate.md#disposed)               | Returns whether the `CaptureVisionRouter` object has been disposed of. |
| [preLoadModule()](./instantiate.md#preloadmodule)   | Loads the specified module to speed up the initialization.             |
| [isModuleLoaded](./instantiate.md#ismoduleloaded)   | Returns whether the specified module has been loaded.                  |

## Single-File Processing

| API Name                                       | Description                                                 |
| ---------------------------------------------- | ----------------------------------------------------------- |
| [capture()](./single-file-processing.md#capture) | Processes an image or file to derive important information. |

## Multiple-File Processing

| API Name                                                                                     | Description                                                                  |
| -------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| [setInput](./multiple-file-processing.md#setinput)                                             | Sets an image source to provide images for consecutive process.              |
| [getInput](./multiple-file-processing.md#getinput)                                             | Returns the image source object.                                             |
| [addCaptureStateListener()](./multiple-file-processing.md#addcapturestatelistener)             | Adds an object that listens to the state changes of the capture process.     |
| [removeCaptureStateListener()](./multiple-file-processing.md#removecapturestatelistener)       | Removes an object which listens to the state changes of the capture process. |
| [addImageSourceStateListener](./multiple-file-processing.md#addimagesourcestatelistener)       | Adds an object that listens to state changes of the image source.            |
| [removeImageSourceStateListener](./multiple-file-processing.md#removeimagesourcestatelistener) | Removes an object which listens to state changes of the image source.        |
| [addResultReceiver()](./multiple-file-processing.md#addresultreceiver)                         | Adds an object as the receiver of captured results.                          |
| [removeResultReceiver()](./multiple-file-processing.md#removeresultreceiver)                   | Removes an object which was added as a receiver of captured results.         |
| [addResultFilter()](./multiple-file-processing.md#addresultfilter)                             | Adds an object as the filter of captured results.                            |
| [startCapturing()](./multiple-file-processing.md#startcapturing)                               | Starts to process images consecutively.                                      |
| [stopCapturing()](./multiple-file-processing.md#stopcapturing)                                 | Stops the consecutive process.                                               |


### Settings

| API Name                                                     | Description                                                                                                   |
| ------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- |
| [initSettings()](./settings.md#initsettings)                   | Initializes settings with either a file or a string.                                                          |
| [outputSettings](./settings.md#outputsettings)                 | Outputs a `CaptureVisionTemplate` specified by its name to a string.                                          |
| [getSimplifiedSettings()](./settings.md#getsimplifiedsettings) | Returns a `SimplifiedCaptureVisionSettings` object for manipulating a specified `CaptureVisionTemplate`.      |
| [updateSettings()](./settings.md#updatesettings)               | Updates a specified `CaptureVisionTemplate` with updated an updated `SimplifiedCaptureVisionSettings` object. |
| [resetSettings()](./settings.md#resetsettings)                 | Resets settings to factory default.                                                                           |

## Intermediate Result

| API Name                                                                            | Description                                    |
| ----------------------------------------------------------------------------------- | ---------------------------------------------- |
| [getIntermediateResultManager](./intermediate-result.md#getintermediateresultmanager) | Returns an `IntermediateResultManager` object. |

### Auxiliary

| API Name                                      | Description |
| --------------------------------------------- | ----------- |
| [getVersion](./auxiliary-methods.md#getversion) | Returns the version of the library including the detailed version numbers of the engine and the main JavaScript code. |

## Interfaces and Enums

In order to make the code more predictable and readable, the library defines a series of supporting interfaces and enumerations:

### Interfaces

* [CaptureStateListener](./interfaces/capture-state-listener.md)
* [ImageSourceStateListener](./interfaces/image-source-state-listener.md)
* [SimplifiedCaptureVisionSettings](./interfaces/simplified-capture-vision-settings.md)

### Enums

* [EnumImageSourceState]({{ site.enums }}core/image-source-state.html?lang=js)
* [EnumPresetTemplate]({{ site.enums }}capture-vision-router/preset-template.html?lang=js)
* [EnumCaptureState]({{ site.enums }}capture-vision-router/capture-state.html?lang=js)