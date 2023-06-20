---
layout: default-layout
title: CaptureVisionRouter Consecutive Process - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to Consecutive Process of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, Consecutive Process, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
permalink: /programming/javascript/api-reference/capture-vision-router/consecutive-process.html
---

# Javascript API Reference - Consecutive Process

| API Name                                                          | Description                                                                  |
| ----------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| [setInput](#setinput)                                             | Sets an image source to provide images for consecutive process.              |
| [addCaptureStateListener()](#addcapturestatelistener)             | Adds an object that listens to the state changes of the capture process.     |
| [removeCaptureStateListener()](#removecapturestatelistener)       | Removes an object which listens to the state changes of the capture process. |
| [addImageSourceStateListener](#addimagesourcestatelistener)       | Adds an object that listens to state changes of the image source.            |
| [removeImageSourceStateListener](#removeimagesourcestatelistener) | Removes an object which listens to state changes of the image source.        |
| [addResultReceiver()](#addresultreceiver)                         | Adds an object as the receiver of captured results.                          |
| [removeResultReceiver()](#removeresultreceiver)                   | Removes an object which was added as a receiver of captured results.         |
| [startCapturing()](#startcapturing)                               | Starts to process images consecutively.                                      |
| [stopCapturing()](#stopcapturing)                                 | Stops the consecutive process.                                               |

## createInstance

Initializes a new instance of the `CaptureVisionRouter` class.

```typescript
Dynamsoft.CVR.CaptureVisionRouter.createInstance: () => Promise<CaptureVisionRouter>;
```

### Return value

A promise that resolves to the initalized `CaptureVisionRouter` object.

### Code Snippet

```js
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
```

## setInput

Sets an image source to provide images for consecutive process.

## addCaptureStateListener()

Adds an object that listens to the state changes of the capture process.

## removeCaptureStateListener()

Removes an object which listens to the state changes of the capture process.

## addImageSourceStateListener

Adds an object that listens to state changes of the image source.

## removeImageSourceStateListener

Removes an object which listens to state changes of the image source.

## addResultReceiver()

Adds an object as the receiver of captured results.

## removeResultReceiver()

Removes an object which was added as a receiver of captured results.

## startCapturing()

Starts to process images consecutively.

## stopCapturing()

Stops the consecutive process.
