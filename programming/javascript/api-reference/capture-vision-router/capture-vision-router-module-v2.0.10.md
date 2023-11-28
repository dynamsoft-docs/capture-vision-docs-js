---
layout: default-layout
title: CaptureVisionRouter Module v2.0.10 - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to CaptureVisionRouter v2.0.10 of Dynamsoft Capture Vision JavaScript Edition as a module.
keywords: capture vision, module, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: CaptureVisionRouter Module
permalink: /programming/javascript/api-reference/capture-vision-router/capture-vision-router-module-v2.0.10.html
---

# CaptureVisionRouter Module

The CaptureVisionRouter module is defined in the namespace `Dynamsoft.CVR`. It consists of the classes `CaptureVisionRouterModule`, `CaptureVisionRouter` and a few interfaces and enumerations.

## CaptureVisionRouterModule Class

This class defines common functionality in the `CaptureVisionRouter` module.

| API Name                                                                                          | Description                                                         |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `static` [getVersion()](./capture-vision-router-module-class-v2.0.10.md#getversion)               | Returns the version of the `CaptureVisionRouter` module.            |
| `static` [engineResourcePath](./capture-vision-router-module-class-v2.0.10.md#engineresourcepath) | Sets or returns the path to find the resources files (.wasm, etc.). |

## CaptureVisionRouter Class

The `CaptureVisionRouter` class defines how a user interacts with image-processing and semantic-processing products in their applications. A `CaptureVisionRouter` instance accepts and processes images from an image source and returns processing results of many types. Read [Final results]({{site.architecture}}output.html#final-results?lang=js) for more information. The following code snippet shows its basic usage:

```typescript
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

| API Name                                                           | Description                                                              |
| ------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `static` [detectEnvironment()](./instantiate.md#detectenvironment) | Detect the current environment.                                          |
| `static` [onWarning](./instantiate.md#onwarning)                   | A callback which is triggered when the running environment is not ideal. |
| `static` [preLoadModule()](./instantiate.md#preloadmodule)         | Loads the specified module to speed up the initialization.               |
| `static` [isModuleLoaded()](./instantiate.md#ismoduleloaded)       | Returns whether the specified module has been loaded.                    |
| `static` [createInstance()](./instantiate.md#createinstance)       | Initializes a new instance of the `CaptureVisionRouter` class.           |
| [dispose()](./instantiate.md#dispose)                              | Releases all resources used by the `CaptureVisionRouter` object.         |
| [disposed](./instantiate.md#disposed)                              | Returns whether the `CaptureVisionRouter` object has been disposed of.   |

### Single-File Processing

| API Name                                          | Description                                                 |
| ------------------------------------------------- | ----------------------------------------------------------- |
| [capture()](./single-image-processing.md#capture) | Processes an image or file to derive important information. |

### Multiple-File Processing

| API Name                                                                                          | Description                                                           |
| ------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| [setInput()](./multiple-image-processing.md#setinput)                                             | Sets an image source to provide images for consecutive process.       |
| [getInput()](./multiple-image-processing.md#getinput)                                             | Returns the image source object.                                      |
| [addImageSourceStateListener()](./multiple-image-processing.md#addimagesourcestatelistener)       | Adds an object that listens to state changes of the image source.     |
| [removeImageSourceStateListener()](./multiple-image-processing.md#removeimagesourcestatelistener) | Removes an object which listens to state changes of the image source. |
| [addResultReceiver()](./multiple-image-processing.md#addresultreceiver)                           | Adds an object as the receiver of captured results.                   |
| [removeResultReceiver()](./multiple-image-processing.md#removeresultreceiver)                     | Removes an object which was added as a receiver of captured results.  |
| [addResultFilter()](./multiple-image-processing.md#addresultfilter)                               | Adds an object as the filter of captured results.                     |
| [removeResultFilter()](./multiple-image-processing.md#removeresultfilter)                         | Removes a result filter for filtering non-essential results.          |
| [startCapturing()](./multiple-image-processing.md#startcapturing)                                 | Starts to process images consecutively.                               |
| [stopCapturing()](./multiple-image-processing.md#stopcapturing)                                   | Stops the consecutive process.                                        |

### Settings

| API Name                                                       | Description                                                                                                   |
| -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| [initSettings()](./settings.md#initsettings)                   | Initializes settings with either a file or a string.                                                          |
| [outputSettings()](./settings.md#outputsettings)               | Outputs a `CaptureVisionTemplate` specified by its name to a string.                                          |
| [getSimplifiedSettings()](./settings.md#getsimplifiedsettings) | Returns a `SimplifiedCaptureVisionSettings` object for manipulating a specified `CaptureVisionTemplate`.      |
| [updateSettings()](./settings.md#updatesettings)               | Updates a specified `CaptureVisionTemplate` with updated an updated `SimplifiedCaptureVisionSettings` object. |
| [resetSettings()](./settings.md#resetsettings)                 | Resets settings to factory default.                                                                           |

### Interfaces

* [ImageSourceStateListener](./interfaces/image-source-state-listener.md)
* [SimplifiedCaptureVisionSettings](./interfaces/simplified-capture-vision-settings.md)

### Enums

* [EnumImageSourceState]({{ site.enums }}core/image-source-state.html?lang=js)
* [EnumPresetTemplate]({{ site.enums }}capture-vision-router/preset-template.html?lang=js)
