---
layout: default-layout
title: CaptureVisionRouter v2.0.10 Consecutive Process - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to Consecutive Process of Dynamsoft Capture Vision JavaScript Edition v2.0.10.
keywords: capture vision, Consecutive Process, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: CVR JavaScript CaptureVisionRouter
---

# CaptureVisionRouter Multiple Image Processing

| Name                                                           | Description                                                                      |
| ------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| [setInput()](#setinput)                                             | Sets an image source to provide images for consecutive process.                  |
| [getInput()](#getinput)                                             | Gets an image source to provide images for consecutive process.                  |
| [addResultReceiver()](#addresultreceiver)                           | Adds an object as the receiver of captured results.                              |
| [removeResultReceiver()](#removeresultreceiver)                     | Removes an object which was added as a receiver of captured results.             |
| [addResultFilter()](#addresultfilter)                               | Adds a result filter to the capture process for filtering non-essential results. |
| [removeResultFilter()](#removeresultfilter)                         | Removes a result filter for filtering non-essential results.                     |
| [startCapturing()](#startcapturing)                                 | Initiates a capturing process based on a specified template.                                          |
| [stopCapturing()](#stopcapturing)                                   | Stops the capturing process.                                                   |

<!-- | [addImageSourceStateListener()](#addimagesourcestatelistener)       | Adds an object that listens to state changes of the image source.                |
| [removeImageSourceStateListener()](#removeimagesourcestatelistener) | Removes an object which listens to state changes of the image source.            | -->

## setInput

Sets the input image source for consecutive process.

**Syntax**

```typescript
setInput(imageSource: Core.ImageSourceAdapter): void;
```

**Parameters**

`imageSource`: The image source adapter object representing the input image source.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let view = await Dynamsoft.DCE.CameraView.createInstance();
cameraEnhancer = await Dynamsoft.DCE.CameraEnhancer.createInstance(view);
router.setInput(cameraEnhancer);
```

## getInput

Returns the current input image source of the CaptureVisionRouter.

**Syntax**

```typescript
getInput(): Core.ImageSourceAdapter;
```

**Parameters**

None.

**Return Value**

Returns the current image source adapter object representing the input image source.

**Code snippet**

```javascript
const imageSource = CaptureVisionRouter.getInput();
```
<!--
## addCaptureStateListener

Adds an object that listens to the state changes of the capture process.

**Syntax**

```typescript
addCaptureStateListener(listener: CaptureStateListener): void;
```

**Parameters**

`listener`: The capture state listener object to be added.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let csl = {
            onCaptureStateChanged(state) {
                console.log("run CaptureStateListener", state);
            }
        }
router.addCaptureStateListener(csl);
```

## removeCaptureStateListener

Removes an object which listens to the state changes of the capture process.

**Syntax**

```typescript
removeCaptureStateListener(listener: CaptureStateListener): void;
```

**Parameters**

`listener`: The capture state listener object to be added.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let csl = {
            onCaptureStateChanged(state) {
                console.log("run CaptureStateListener", state);
            }
        }
router.removeCaptureStateListener(csl);
```
-->
<!-- 
## addImageSourceStateListener

Adds an object that listens to state changes of the image source.

**Syntax**

```typescript
addImageSourceStateListener(listener: ImageSourceStateListener): void;
```

**Parameters**

`listener`: The listener object, of type `ImageSourceStateListener`.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let listener = {
    onImageSourceStateReceived(state) {
        console.log("run ImageSourceAdapterStatusListener", state);
    }
}
router.addImageSourceStateListener(listener);
```

**See Also**

* [ImageSourceState]({{ site.enums }}core/image-source-state.html?lang=js)

## removeImageSourceStateListener

Removes an object which listens to state changes of the image source.

**Syntax**

```typescript
removeImageSourceStateListener(listener: ImageSourceStateListener): void;
```

**Parameters**

`listener`: The listener object, of type `ImageSourceStateListener`.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let listener = {
    onImageSourceStateReceived(state) {
        console.log("run ImageSourceAdapterStatusListener", state);
    }
}
router.removeImageSourceStateListener(listener);
``` -->

## addResultReceiver

Adds an object as the receiver of captured results.

**Syntax**

```typescript
addResultReceiver(receiver: Core.CapturedResultReceiver): void;
```

**Parameters**

`receiver`: The receiver object, of type `CapturedResultReceiver`.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const resultReceiver = new Dynamsoft.CVR.CapturedResultReceiver();
resultReceiver.onDetectedQuadsReceived(result) {
    //* Do something with the result */
};
router.addResultReceiver(resultReceiver);
```

## removeResultReceiver

Removes an object which was added as a receiver of captured results.

**Syntax**

```typescript
removeResultReceiver(receiver: Core.CapturedResultReceiver): void;
```

**Parameters**

`receiver`: The receiver object, of type `CapturedResultReceiver`.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const resultReceiver = new Dynamsoft.CVR.CapturedResultReceiver();
resultReceiver.onDetectedQuadsReceived(result) {
    //* Do something with the result */
};
router.addResultReceiver(resultReceiver);
router.removeResultReceiver(resultReceiver);
```

## addResultFilter

**Syntax**

```typescript
addResultFilter(filter: MultiFrameResultCrossFilter): Promise<void>;
```

**Parameters**

`filter`: The result filter object to be added.

**Return Value**

Returns a promise that resolves when the result filter have been successfully added.

**Code snippet**

```javascript
filter = new Dynamsoft.Utility.MultiFrameResultCrossFilter();
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
router.addResultReceiver(filter);
```

> In the provided code snippet, the default filter implementation is utilized. This filter can offer cross-validation and de-duplication functionalities. To utilize this filter, it's necessary to include the corresponding package `dynamsoft-utility`.

**See also**

[MultiFrameResultCrossFilter](https://www.dynamsoft.com/capture-vision/docs/web/programming/javascript/api-reference/utility/multi-frame-result-cross-filter.html?product=ddn&repoType=web)

## removeResultFilter

**Syntax**

```typescript
removeResultFilter(filter: MultiFrameResultCrossFilter): void;
```

**Parameters**

`filter`: The result filter object to be removed.

**Return Value**

None.

**Code snippet**

```javascript
filter = new Dynamsoft.Utility.MultiFrameResultCrossFilter();
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
router.addResultReceiver(filter);
router.removeResultFilter(filter);
```

## startCapturing

Initiates a capturing process based on a specified template.

**Syntax**

```typescript
startCapturing(templateName?: string): Promise<void>;
```

**Parameters**

`templateName`: specifies a "CaptureVisionTemplate" to use. If not specified, "Default" is used. There are two types of CaptureVisionTemplates: the [preset ones](./preset-templates.md) which come with the SDK and the custom ones that get initialized when the user calls [initSettings](./settings.md#initsettings). Please be aware that the [preset CaptureVisionTemplates](./preset-templates.md)  will be overwritten if the user calls [initSettings](./settings.md#initsettings) and passes customized settings.

**Return Value**

A promise that resolves when the capturing process has successfully started. It does not provide any value upon resolution.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
await router.startCapturing();
```

## stopCapturing

Stops the capturing process.

**Syntax**

```typescript
stopCapturing(): void;
```

**Parameters**

None.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
router.stopCapturing();
```