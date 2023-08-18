---
layout: default-layout
title: CaptureVisionRouter Consecutive Process - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to Consecutive Process of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, Consecutive Process, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: CVR JavaScript CaptureVisionRouter
permalink: /programming/javascript/api-reference/capture-vision-router/multiple-file-processing.html
---

# CaptureVisionRouterMultiple File Processing

| API Name                                                            | Description                                                                     |
| ------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| [setInput()](#setinput)                                             | Sets an image source to provide images for consecutive process.                 |
| [getInput()](#getinput)                                             | Gets an image source to provide images for consecutive process.                 |
| [addCaptureStateListener()](#addcapturestatelistener)               | Adds an object that listens to the state changes of the capture process.        |
| [removeCaptureStateListener()](#removecapturestatelistener)         | Removes an object which listens to the state changes of the capture process.    |
| [addImageSourceStateListener()](#addimagesourcestatelistener)       | Adds an object that listens to state changes of the image source.               |
| [removeImageSourceStateListener()](#removeimagesourcestatelistener) | Removes an object which listens to state changes of the image source.           |
| [addResultReceiver()](#addresultreceiver)                           | Adds an object as the receiver of captured results.                             |
| [removeResultReceiver()](#removeresultreceiver)                     | Removes an object which was added as a receiver of captured results.            |
| [addResultFilter()](#addresultfilter)                               | Adds a result filter to the capture process for filtering non-essential results.|
| [startCapturing()](#startcapturing)                                 | Starts to process images consecutively.                                         |
| [stopCapturing()](#stopcapturing)                                   | Stops the consecutive process.                                                  |

## setInput

Sets the input image source for consecutive process.

**Syntax**

```typescript
setInput(imageSource: Core.BasicStructures.ImageSourceAdapter): void;
```

**parameter**

`imageSource`: The image source adapter object representing the input image source.

**Return Value**

None.

**Code snippet**

```javascript
cvr = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let view = await Dynamsoft.DCE.CameraView.createInstance();
dce = await Dynamsoft.DCE.CameraEnhancer.createInstance(view);
cvr.setInput(dce);
```

## getInput

Returns the current input image source of the CaptureVisionRouter.

**Syntax**

```typescript
getInput(): Core.BasicStructures.ImageSourceAdapter;
```

**parameter**

None.

**Return Value**

Returns the current image source adapter object representing the input image source.

**Code snippet**

```javascript
const imageSource = CaptureVisionRouter.getInput();
```

## addCaptureStateListener

Adds an object that listens to the state changes of the capture process.

**Syntax**

```typescript
addCaptureStateListener(listener: CaptureStateListener): void;
```

**parameter**

`listener`: The capture state listener object to be added.

**Return Value**

None.

**Code snippet**

```javascript
cvr = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let csl = {
            onCaptureStateChanged(state) {
                console.log("run CaptureStateListener", state);
            }
        }
cvr.addCaptureStateListener(csl);
```

## removeCaptureStateListener

Removes an object which listens to the state changes of the capture process.

**Syntax**

```typescript
removeCaptureStateListener(listener: CaptureStateListener): void;
```

**parameter**

`listener`: The capture state listener object to be added.

**Return Value**

None.

**Code snippet**

```javascript
cvr = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let csl = {
            onCaptureStateChanged(state) {
                console.log("run CaptureStateListener", state);
            }
        }
cvr.removeCaptureStateListener(csl);
```

## addImageSourceStateListener

Adds an object that listens to state changes of the image source.

**Syntax**

```typescript
addImageSourceStateListener(listener: ImageSourceStateListener): void;
```

**parameter**

`listener`: The image source state listener object to be added.

**Return Value**

None.

**Code snippet**

```javascript
cvr = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let isasl = {
            onImageSourceStateListener(state) {
                console.log("run ImageSourceAdapterStatusListener", state);
            }
        }
cvr.addImageSourceStateListener(isasl);
```

## removeImageSourceStateListener

Removes an object which listens to state changes of the image source.

**Syntax**

```typescript
removeImageSourceStateListener(listener: ImageSourceStateListener): void;
```

**parameter**

`listener`: The image source state listener object to be added.

**Return Value**

None.

**Code snippet**

```javascript
cvr = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let isasl = {
            onImageSourceStateListener(state) {
                console.log("run ImageSourceAdapterStatusListener", state);
            }
        }
cvr.removeImageSourceStateListener(isasl);
```

## addResultReceiver

Adds an object as the receiver of captured results.

**Syntax**

```typescript
addResultReceiver(receiver: Core.BasicStructures.CapturedResultReceiver): void;
```

**parameter**

`receiver`: The result receiver object to be added.

**Return Value**

None.

**Code snippet**

```javascript
cvr = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let crr = {
            onCapturedResultReceived(result) {
                console.log(result);
            },
            onDecodedBarcodesReceived(result) {
            }
        };
cvr.addResultReceiver(crr);
```

## removeResultReceiver

Removes an object which was added as a receiver of captured results.

**Syntax**

```typescript
removeResultReceiver(receiver: Core.BasicStructures.CapturedResultReceiver): void;
```

**parameter**

`receiver`: The result receiver object to be added.

**Return Value**

None.

**Code snippet**

```javascript
cvr = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let crr = {
            onCapturedResultReceived(result) {
                console.log(result);
            },
            onDecodedBarcodesReceived(result) {
                console.log(result);
            }
        };
cvr.addResultReceiver(crr);
cvr.removeResultReceiver(crr);
```

## addResultFilter

**Syntax**

```typescript
addResultFilter(filter: Core.BasicStructures.CapturedResultFilter): Promise<void>;
```

**parameter**

`filter`: The result filter object to be added.

**Return Value**

Returns a promise that resolves when the result filter have been successfully added.

**Code snippet**

```javascript
cvr = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
cvr.addResultReceiver(rf);
```

## startCapturing

Starts to process images consecutively.

**Syntax**

```typescript
startCapturing(templateName?: string): void;
```

**parameter**

`templateName (optional)`: The name of the template to use for capturing. If not specified, the default template (`EnumPresetTemplate.PT_DEFAULT`) will be used.

**Return Value**

None.

**Code snippet**

```javascript
cvr = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
cvr.startCapturing();
```

## stopCapturing

Stops the consecutive process.

**Syntax**

```typescript
stopCapturing(): void;
```

**parameter**

None.

**Return Value**

None.

**Code snippet**

```javascript
cvr = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
cvr.stopCapturing();
```