---
layout: default-layout
title: CaptureVisionRouter Module - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to CaptureVisionRouter of Dynamsoft Capture Vision JavaScript Edition as a module.
keywords: capture vision, module, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: CaptureVisionRouter Module
permalink: /programming/javascript/api-reference/capture-vision-router/capture-vision-router-module.html
---
<!-- 2.0.20 -- Updated on 11/28/2023-->

# CaptureVisionRouter Module

The CaptureVisionRouter module is defined in the namespace `Dynamsoft.CVR`. It consists of the classes `CaptureVisionRouterModule`, `CaptureVisionRouter`, `CapturedResultReceiver`, `IntermediateResultReceiver`, `IntermediateResultManager` and a few interfaces and enumerations.

## CaptureVisionRouterModule Class

This class defines common functionality in the `CaptureVisionRouter` module. At present, there is only one API:

| API Name                                                                    | Description                                            |
| --------------------------------------------------------------------------- | ------------------------------------------------------ |
| `static` [getVersion()](./capture-vision-router-module-class.md#getversion) | Returns the version of the CaptureVisionRouter module. |

## CaptureVisionRouter Class

The `CaptureVisionRouter` class defines how a user interacts with image-processing and semantic-processing products in their applications. A `CaptureVisionRouter` instance accepts and processes images from an image source and returns processing results which may contain [Final results]({{site.architecture}}output.html#final-results?lang=js){:target="_blank"} or [Intermediate Results]({{site.architecture}}output.html#intermediate-results?lang=js){:target="_blank"}.

The APIs for this class are:

### Create and Destroy Instances

| API Name                                                     | Description                                                            |
| ------------------------------------------------------------ | ---------------------------------------------------------------------- |
| `static` [createInstance()](./instantiate.md#createinstance) | Initializes a new instance of the `CaptureVisionRouter` class.         |
| [dispose()](./instantiate.md#dispose)                        | Releases all resources used by the `CaptureVisionRouter` object.       |
| [disposed](./instantiate.md#disposed)                        | Returns whether the `CaptureVisionRouter` object has been disposed of. |

### Single-Image Processing

| API Name                                          | Description                                                 |
| ------------------------------------------------- | ----------------------------------------------------------- |
| [capture()](./single-image-processing.md#capture) | Processes an image or file to derive important information. |

### Multiple-Image Processing

| API Name                                                                                          | Description                                                                                |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| [setInput()](./multiple-image-processing.md#setinput)                                             | Sets up an image source to provide images for continuous processing.                       |
| [getInput()](./multiple-image-processing.md#getinput)                                             | Returns the image source object.                                                           |
| [addImageSourceStateListener()](./multiple-image-processing.md#addimagesourcestatelistener)       | Adds an `ImageSourceStateListener` object that listens to state changes of the image source. |
| [removeImageSourceStateListener()](./multiple-image-processing.md#removeimagesourcestatelistener) | Removes the specified `ImageSourceStateListener` object.                                     |
| [addResultReceiver()](./multiple-image-processing.md#addresultreceiver)                           | Adds a `CapturedResultReceiver` object as the receiver of captured results.                  |
| [removeResultReceiver()](./multiple-image-processing.md#removeresultreceiver)                     | Removes the specified `CapturedResultReceiver` object.                                       |
| [addResultFilter()](./multiple-image-processing.md#addresultfilter)                               | Adds a `CapturedResultFilter` object to filter non-essential results.                        |
| [removeResultFilter()](./multiple-image-processing.md#removeresultfilter)                         | Removes the specified `CapturedResultFilter` object.                                         |
| [startCapturing()](./multiple-image-processing.md#startcapturing)                                 | Starts to process images consecutively.                                                    |
| [stopCapturing()](./multiple-image-processing.md#stopcapturing)                                   | Stops the consecutive process.                                                             |

<!-- Not required at this time -> meant for Panorama
| [addCaptureStateListener()](./multiple-image-processing.md#addresultfilter)                       | Adds a CaptureStateListener object to listen to the state changes of the capture process.  |
| [removeCaptureStateListener()](./multiple-image-processing.md#removeresultfilter)                 | Removes the specified CaptureStateListener object.                                         | -->

### Settings

| API Name                                                       | Description                                                                                                   |
| -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| [initSettings()](./settings.md#initsettings)                   | Initializes settings with either a file or a string.                                                          |
| [outputSettings()](./settings.md#outputsettings)               | Outputs a `CaptureVisionTemplate` specified by its name to a string.                                          |
| [getSimplifiedSettings()](./settings.md#getsimplifiedsettings) | Returns a `SimplifiedCaptureVisionSettings` object for manipulating a specified `CaptureVisionTemplate`.      |
| [updateSettings()](./settings.md#updatesettings)               | Updates a specified `CaptureVisionTemplate` with an updated `SimplifiedCaptureVisionSettings` object. |
| [resetSettings()](./settings.md#resetsettings)                 | Resets settings to factory default.                                                                           |

### Intermediate Result

| API Name                                                                                | Description                                    |
| --------------------------------------------------------------------------------------- | ---------------------------------------------- |
| [getIntermediateResultManager()](./intermediate-result.md#getintermediateresultmanager) | Returns an `IntermediateResultManager` object. |

## IntermediateResultManager Class

The `IntermediateResultManager` class enables the user to communicate with the `CaptureVisionRouter` class regarding intermediate results.

The APIs for this class are:

| API Name                                                                      | Description                              |
| ----------------------------------------------------------------------------- | ---------------------------------------- |
| [addResultReceiver()](./intermediate-result-manager.md#addresultreceiver)       | Adds an intermediate result receiver.    |
| [removeResultReceiver()](./intermediate-result-manager.md#removeresultreceiver) | Removes an intermediate result receiver. |

## Interfaces

<!-- * [CapturedResultFilter](./interfaces/captured-result-filter.md) -->
* [CapturedResultReceiver](./interfaces/captured-result-receiver.md)
* [IntermediateResultReceiver](./interfaces/intermediate-result-receiver.md)
* [ImageSourceStateListener](./interfaces/image-source-state-listener.md)
* [SimplifiedCaptureVisionSettings](./interfaces/simplified-capture-vision-settings.md)

<!-- not required at the moment, meant for panorama
  * [CaptureStateListener] -->

## Enums

* [EnumImageSourceState]({{ site.enums }}core/image-source-state.html?lang=js)

<!-- 
* [EnumPresetTemplate]({{ site.enums }}capture-vision-router/preset-template.html?lang=js)

not required at the moment, meant for panorama
  * [EnumCaptureState]({{ site.enums }}capture-vision-router/capture-state.html?lang=js) -->
