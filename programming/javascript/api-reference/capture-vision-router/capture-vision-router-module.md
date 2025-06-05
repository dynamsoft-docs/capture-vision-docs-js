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

# DynamsoftCaptureVisionRouter Module

The CaptureVisionRouter module is defined in the namespace `Dynamsoft.CVR`. It consists of the classes `CaptureVisionRouter`, `CaptureVisionRouterModule`, `CapturedResultReceiver`, `IntermediateResultManager`, `IntermediateResultReceiver` and a few interfaces and enumerations.

## CaptureVisionRouter Class

The `CaptureVisionRouter` class defines how a user interacts with image-processing and semantic-processing products in their applications. A `CaptureVisionRouter` instance accepts and processes images from an image source and returns processing results which may contain [Final results]({{site.dcvb_architecture}}output.html#final-results?lang=js){:target="_blank"} or [Intermediate Results]({{site.dcvb_architecture}}output.html#intermediate-results?lang=js){:target="_blank"}.

### Create and Destroy Instances

| Name                                                         | Description                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `static` [createInstance()](./instantiate.md#createinstance) | Initializes a new instance of the `CaptureVisionRouter` class.           |
| [dispose()](./instantiate.md#dispose)                        | Releases all resources used by the `CaptureVisionRouter` instance.       |
| [disposed](./instantiate.md#disposed)                        | Returns whether the `CaptureVisionRouter` instance has been disposed of. |

### Single-Image Processing

| Name                                              | Description                                                                                   |
| ------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| [capture()](./single-image-processing.md#capture) | Processes a single image or a file containing a single image to derive important information. |

### Multiple-Image Processing

| Name                                                                          | Description                                                                  |
| ----------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| [setInput()](./multiple-image-processing.md#setinput)                         | Sets up an image source to provide images for continuous processing.         |
| [getInput()](./multiple-image-processing.md#getinput)                         | Returns the image source object.                                             |
| [addResultReceiver()](./multiple-image-processing.md#addresultreceiver)       | Adds a `CapturedResultReceiver` object as the receiver of captured results.  |
| [removeResultReceiver()](./multiple-image-processing.md#removeresultreceiver) | Removes the specified `CapturedResultReceiver` object.                       |
| [addResultFilter()](./multiple-image-processing.md#addresultfilter)           | Adds a `MultiFrameResultCrossFilter` object to filter non-essential results. |
| [removeResultFilter()](./multiple-image-processing.md#removeresultfilter)     | Removes the specified `MultiFrameResultCrossFilter` object.                  |
| [startCapturing()](./multiple-image-processing.md#startcapturing)             | Initiates a capturing process based on a specified template.                 |
| [stopCapturing()](./multiple-image-processing.md#stopcapturing)               | Stops the capturing process.                                                 |

<!-- | [addImageSourceStateListener()](./multiple-image-processing.md#addimagesourcestatelistener)       | Adds an `ImageSourceStateListener` object that monitors changes in the state of an image source. |
| [removeImageSourceStateListener()](./multiple-image-processing.md#removeimagesourcestatelistener) | Removes the specified `ImageSourceStateListener` object.                                     | -->
<!-- Not required at this time -> meant for Panorama
| [addCaptureStateListener()](./multiple-image-processing.md#addresultfilter)                       | Adds a CaptureStateListener object to listen to the state changes of the capture process.  |
| [removeCaptureStateListener()](./multiple-image-processing.md#removeresultfilter)                 | Removes the specified CaptureStateListener object.                                         | -->

### Settings

| Name                                                           | Description                                                                                                                  |
| -------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| [initSettings()](./settings.md#initsettings)                   | Initializes settings with either a file or a string.                                                                         |
| [outputSettings()](./settings.md#outputsettings)               | Outputs a `CaptureVisionTemplate` specified by its name to a string.                                                         |
| [outputSettingsToFile](./settings.md#outputsettingstofile)     | Generates a Blob object or initiates a JSON file download containing the settings for the specified `CaptureVisionTemplate`. |
| [getSimplifiedSettings()](./settings.md#getsimplifiedsettings) | Retrieves a JSON object that contains simplified settings for the specified `CaptureVisionTemplate`.                         |
| [getTemplateNames()](./settings.md#gettemplatenames)           | Retrieves the names of all the currently available templates.                         |
| [updateSettings()](./settings.md#updatesettings)               | Updates the specified `CaptureVisionTemplate` with an updated `SimplifiedCaptureVisionSettings` object.                      |
| [resetSettings()](./settings.md#resetsettings)                 | Restores all runtime settings to their original default values.                                                              |

### Intermediate Result

| Name                                                                                    | Description                                                                                |
| --------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| [getIntermediateResultManager()](./intermediate-result.md#getintermediateresultmanager) | Returns an object, of type `IntermediateResultManager`, that manages intermediate results. |

### Auxiliaries

| Name                                                                                    | Description                                                                                |
| --------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| [maxImageSideLength](./auxiliary.md#maximagesidelength)                        | Limits the maximum pixel value of the longest side of an image during the processing workflow.       |
| [appendModelBuffer()](./auxiliary.md#appendmodelbuffer)                        | Loads a specific data file containing recognition information.       |
| [onDataLoadProgressChanged()](./auxiliary.md#ondataloadprogresschanged)                        | An event that fires during the loading of a recognition data file (.data). |
| [onCaptureError()](./auxiliary.md#oncaptureerror)                        | An event that fires when an error occurs from the start of capturing process. |

## CaptureVisionRouterModule Class

The `CaptureVisionRouterModule` class defines common functionality in the `CaptureVisionRouter` module.

| Name                                                                        | Description                                            |
| --------------------------------------------------------------------------- | ------------------------------------------------------ |
| `static` [getVersion()](./capture-vision-router-module-class.md#getversion) | Returns the version of the CaptureVisionRouter module. |

## CapturedResultReceiver Class

The `CapturedResultReceiver` class is designed as a standardized way for retrieving captured results in the Dynamsoft Capture Vision architecture. It adopts an event-driven approach, with events dedicated to various result types, such as the original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results, etc.

| Name                                                                                           | Description                                                  |
| ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| [onCapturedResultReceived()](./captured-result-receiver.md#oncapturedresultreceived)           | Event triggered when a generic captured result is available. |
| [onOriginalImageResultReceived()](./captured-result-receiver.md#onoriginalimageresultreceived) | Event triggered when the original image result is available. |
| [onDecodedBarcodesReceived()](./captured-result-receiver.md#ondecodedbarcodesreceived)         | Event triggered when decoded barcodes are available.         |
| [onRecognizedTextLinesReceived()](./captured-result-receiver.md#onrecognizedtextlinesreceived) | Event triggered when recognized text lines are available.    |
| [onDetectedQuadsReceived()](./captured-result-receiver.md#ondetectedquadsreceived)             | Event triggered when detected quads are available.           |
| [onNormalizedImagesReceived()](./captured-result-receiver.md#onnormalizedimagesreceived)       | Event triggered when normalized images are available.        |
| [onParsedResultsReceived()](./captured-result-receiver.md#onparsedresultsreceived)             | Event triggered when parsed results are available.           |

## IntermediateResultManager Class

The `IntermediateResultManager` class is responsible for handling intermediate results obtained during the process of an image. It offers methods to both register and deregister receivers of these intermediate results, as well as to retrieve the original image data.

| Name                                                                            | Description                                                                         |
| ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| [addResultReceiver()](./intermediate-result-manager.md#addresultreceiver)       | Adds a `IntermediateResultReceiver` object as the receiver of intermediate results. |
| [removeResultReceiver()](./intermediate-result-manager.md#removeresultreceiver) | Removes the specified `IntermediateResultReceiver` object.                          |
| [getOriginalImage()](./intermediate-result-manager.md#getoriginalimage)         | Retrieves the original image data.                                                  |

## IntermediateResultReceiver Class

The `IntermediateResultReceiver` class is designed as a standardized way for retrieving intermediate results in image processing workflows in the Dynamsoft Capture Vision architecture. It adopts an event-driven approach, with events triggered for specific types of results, such as pre-detected regions, localized barcodes, etc. Each event is optional, allowing flexibility and customization based on the needs of the application.

| Name                                                                                                                               | Description                                                                 |
| ---------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| [onTaskResultsReceived()](./intermediate-result-receiver.md#ontaskresultsreceived)                                                 | Event triggered when task results are received.                             |
| [onPredetectedRegionsReceived()](./intermediate-result-receiver.md#onpredetectedregionsreceived)                                   | Event triggered when pre-detected regions are received.                     |
| [onLocalizedBarcodesReceived()](./intermediate-result-receiver.md#onlocalizedbarcodesreceived)                                     | Event triggered when localized barcodes are received.                       |
| [onDecodedBarcodesReceived()](./intermediate-result-receiver.md#ondecodedbarcodesreceived)                                         | Event triggered when decoded barcodes are received.                         |
| [onLocalizedTextLinesReceived()](./intermediate-result-receiver.md#onlocalizedtextlinesreceived)                                   | Event triggered when localized text lines are received.                     |
| [onRecognizedTextLinesReceived()](./intermediate-result-receiver.md#onrecognizedtextlinesreceived)                                 | Event triggered when recognized text lines are received.                    |
| [onDetectedQuadsReceived()](./intermediate-result-receiver.md#ondetectedquadsreceived)                                             | Event triggered when detected quads are received.                           |
| [onNormalizedImagesReceived()](./intermediate-result-receiver.md#onnormalizedimagesreceived)                                       | Event triggered when normalized images are received.                        |
| [onColourImageUnitReceived()](./intermediate-result-receiver.md#oncolourimageunitreceived)                                         | Event triggered when a colour image unit is received.                       |
| [onScaledDownColourImageUnitReceived()](./intermediate-result-receiver.md#onscaleddowncolourimageunitreceived)                     | Event triggered when a scaled-down colour image unit is received.           |
| [onGrayscaleImageUnitReceived()](./intermediate-result-receiver.md#ongrayscaleimageunitreceived)                                   | Event triggered when a grayscale image unit is received.                    |
| [onTransformedGrayscaleImageUnitReceived()](./intermediate-result-receiver.md#ontransformedgrayscaleimageunitreceived)             | Event triggered when a transformed grayscale image unit is received.        |
| [onEnhancedGrayscaleImageUnitReceived()](./intermediate-result-receiver.md#onenhancedgrayscaleimageunitreceived)                   | Event triggered when an enhanced grayscale image unit is received.          |
| [onBinaryImageUnitReceived()](./intermediate-result-receiver.md#onbinaryimageunitreceived)                                         | Event triggered when a binary image unit is received.                       |
| [onTextureDetectionResultUnitReceived()](./intermediate-result-receiver.md#ontexturedetectionresultunitreceived)                   | Event triggered when a texture detection result unit is received.           |
| [onTextureRemovedGrayscaleImageUnitReceived()](./intermediate-result-receiver.md#ontextureremovedgrayscaleimageunitreceived)       | Event triggered when a texture-removed grayscale image unit is received.    |
| [onTextureRemovedBinaryImageUnitReceived()](./intermediate-result-receiver.md#ontextureremovedbinaryimageunitreceived)             | Event triggered when a texture-removed binary image unit is received.       |
| [onContoursUnitReceived()](./intermediate-result-receiver.md#oncontoursunitreceived)                                               | Event triggered when a contours unit is received.                           |
| [onLineSegmentsUnitReceived()](./intermediate-result-receiver.md#onlinesegmentsunitreceived)                                       | Event triggered when a line segments unit is received.                      |
| [onTextZonesUnitReceived()](./intermediate-result-receiver.md#ontextzonesunitreceived)                                             | Event triggered when a text zones unit is received.                         |
| [onTextRemovedBinaryImageUnitReceived()](./intermediate-result-receiver.md#ontextremovedbinaryimageunitreceived)                   | Event triggered when a text-removed binary image unit is received.          |
| [onLongLinesUnitReceived()](./intermediate-result-receiver.md#onlonglinesunitreceived)                                             | Event triggered when a long lines unit is received.                         |
| [onCornersUnitReceived()](./intermediate-result-receiver.md#oncornersunitreceived)                                                 | Event triggered when a corners unit is received.                            |
| [onCandidateQuadEdgesUnitReceived()](./intermediate-result-receiver.md#oncandidatequadedgesunitreceived)                           | Event triggered when a candidate quad edges unit are detected.              |
| [onCandidateBarcodeZonesUnitReceived()](./intermediate-result-receiver.md#oncandidatebarcodezonesunitreceived)                     | Event triggered when a candidate barcode zones unit are detected.           |
| [onScaledUpBarcodeImageUnitReceived()](./intermediate-result-receiver.md#onscaledupbarcodeimageunitreceived)                       | Event triggered when a scaled-up barcode image unit is received.            |
| [onDeformationResistedBarcodeImageUnitReceived()](./intermediate-result-receiver.md#ondeformationresistedbarcodeimageunitreceived) | Event triggered when a deformation-resisted barcode image unit is received. |
| [onComplementedBarcodeImageUnitReceived()](./intermediate-result-receiver.md#oncomplementedbarcodeimageunitreceived)               | Event triggered when a complemented barcode image unit is received.         |

## BufferedItemsManager Class

The `BufferedItemsManager` class is responsible for storing sample data generated during the recognition of confusable characters. Users can obtain these images and reuse them for more precise recognition in the future.

| Name                                                                                     | Description                                   |
| ---------------------------------------------------------------------------------------- | --------------------------------------------- |
| [getMaxBufferedItems()](./buffered-items-manager.md#getmaxbuffereditems)                 | Gets the buffered recognized character items. |
| [setMaxBufferedItems()](./buffered-items-manager.md#setmaxbuffereditems)                 | Sets the maximum number of buffered items.    |
| [getBufferedCharacterItemSet()](./buffered-items-manager.md#getbufferedcharacteritemset) | Gets the buffered recognized character items. |

## Interfaces

* [CapturedResult](./interfaces/captured-result.md)
* [SimplifiedCaptureVisionSettings](./interfaces/simplified-capture-vision-settings.md)

<!-- has bug, ignore for now * [ImageSourceStateListener](./interfaces/image-source-state-listener.md) -->

<!-- not useful at present
  * [CapturedResultReceiver](./interfaces/captured-result-receiver.md) -->
<!-- not required at the moment, meant for panorama
  * [CaptureStateListener] -->

## Enums

* [EnumImageSourceState]({{ site.dcvb_enums }}core/image-source-state.html?lang=js)

<!-- 
* [EnumPresetTemplate]({{ site.enums }}capture-vision-router/preset-template.html?lang=js)

not required at the moment, meant for panorama
  * [EnumCaptureState]({{ site.enums }}capture-vision-router/capture-state.html?lang=js) -->
