---
layout: default-layout
title: CaptureVisionRouter Consecutive Process - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to Consecutive Process of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, Consecutive Process, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: CVR JavaScript CaptureVisionRouter
---

# CaptureVisionRouter Multiple Image Processing

| Name                                            | Description                                                                  |
| ----------------------------------------------- | ---------------------------------------------------------------------------- |
| [setInput()](#setinput)                         | Sets up an image source to provide images for continuous processing.         |
| [getInput()](#getinput)                         | Returns the image source object.                                             |
| [addResultReceiver()](#addresultreceiver)       | Adds a `CapturedResultReceiver` object as the receiver of captured results.  |
| [removeResultReceiver()](#removeresultreceiver) | Removes the specified `CapturedResultReceiver` object.                       |
| [addResultFilter()](#addresultfilter)           | Adds a `MultiFrameResultCrossFilter` object to filter non-essential results. |
| [removeResultFilter()](#removeresultfilter)     | Removes the specified `MultiFrameResultCrossFilter` object.                  |
| [startCapturing()](#startcapturing)             | Initiates a capturing process based on a specified template.                 |
| [stopCapturing()](#stopcapturing)               | Stops the capturing process.                                               |

<!-- 
| [addImageSourceStateListener()](#addimagesourcestatelistener)       | Adds an `ImageSourceStateListener` object that monitors changes in the state of an image source. |
| [removeImageSourceStateListener()](#removeimagesourcestatelistener) | Removes the specified `ImageSourceStateListener` object.                                     | -->
<!-- 
| [addCaptureStateListener()](#addcapturestatelistener)               | Adds a CaptureStateListener object to listen to the state changes of the capture process.  |
| [removeCaptureStateListener()](#removecapturestatelistener)         | Removes the specified CaptureStateListener object.                                         | -->

## setInput

Sets up an image source to provide images for continuous processing.

**Syntax**

```typescript
setInput(imageSource: ImageSourceAdapter): void;
```

**Parameters**

`imageSource`: The image source which is compliant with the `ImageSourceAdapter` interface.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let view = await Dynamsoft.DCE.CameraView.createInstance();
cameraEnhancer = await Dynamsoft.DCE.CameraEnhancer.createInstance(view);
router.setInput(cameraEnhancer);
```

**See Also**

[ImageSourceAdapter](../core/image-source-adapter.md)

## getInput

Returns the image source object.

**Syntax**

```typescript
getInput(): ImageSourceAdapter;
```

**Parameters**

None.

**Return Value**

Returns the current image source.

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

Adds an `ImageSourceStateListener` object that monitors changes in the state of an image source.

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

## removeImageSourceStateListener

Removes the specified `ImageSourceStateListener` object.

**Syntax**

```typescript
removeImageSourceStateListener(listener: ImageSourceStateListener): boolean;
```

**Parameters**

`listener`: The listener object, of type `ImageSourceStateListener`.

**Return Value**

Boolean indicating whether the operation succeeded.

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

Adds a `CapturedResultReceiver` object as the receiver of captured results.

**Syntax**

```typescript
addResultReceiver(receiver: CapturedResultReceiver): void;
```

**Parameters**

`receiver`: The receiver object, of type `CapturedResultReceiver`.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const resultReceiver = new Dynamsoft.CVR.CapturedResultReceiver();
resultReceiver.onCapturedResultReceived = (result) => {
    /* Do something with the result */
};
router.addResultReceiver(resultReceiver);
```

## removeResultReceiver

Removes the specified `CapturedResultReceiver` object.

**Syntax**

```typescript
removeResultReceiver(receiver: CapturedResultReceiver): void;
```

**Parameters**

`receiver`: The receiver object, of type `CapturedResultReceiver`.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const resultReceiver = new Dynamsoft.CVR.CapturedResultReceiver();
resultReceiver.onCapturedResultReceived = (result) => {
    /* Do something with the result */
};
router.addResultReceiver(resultReceiver);
//...
router.removeResultReceiver(resultReceiver);
```

## addResultFilter

Adds a `MultiFrameResultCrossFilter` object to filter non-essential results.

**Syntax**

```typescript
addResultFilter(filter: MultiFrameResultCrossFilter): Promise<void>;
```

**Parameters**

`filter`: The filter object, of type `MultiFrameResultCrossFilter`.

**Return Value**

A promise that resolves when the operation has successfully completed. It does not provide any value upon resolution.

**Code snippet**

```javascript
filter = new Dynamsoft.Utility.MultiFrameResultCrossFilter();
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
router.addResultFilter(filter);
```

> In the provided code snippet, the default filter implementation is utilized. This filter can offer cross-validation and de-duplication functionalities. To utilize this filter, it's necessary to include the corresponding package `dynamsoft-utility`.

**See also**

[MultiFrameResultCrossFilter](https://www.dynamsoft.com/capture-vision/docs/web/programming/javascript/api-reference/utility/multi-frame-result-cross-filter.html?product=ddn&repoType=web)

## removeResultFilter

Removes the specified `MultiFrameResultCrossFilter` object.

**Syntax**

```typescript
removeResultFilter(filter: MultiFrameResultCrossFilter): : Promise<void>;
```

**Parameters**

`filter`: The filter object, of type `MultiFrameResultCrossFilter`.

**Return Value**

A promise that resolves when the operation has successfully completed. It does not provide any value upon resolution.

**Code snippet**

```javascript
filter = new Dynamsoft.Utility.MultiFrameResultCrossFilter();
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
router.addResultFilter(filter);
// ...
router.removeResultFilter(filter);
```

## startCapturing

Initiates a capturing process based on a specified template. This process is repeated for each image fetched from the source.

**Syntax**

```typescript
startCapturing(templateName?: string): Promise<void>;
```

**Parameters**

`templateName`: specifies a "CaptureVisionTemplate" to use. If not specified, "Default" is used. There are two types of CaptureVisionTemplates: the [built-in ones](./built-in-templates.md) which come with the SDK and the custom ones that get initialized when the user calls [initSettings](./settings.md#initsettings). Please be aware that the [built-in CaptureVisionTemplates](./built-in-templates.md) will be overwritten should the user calls [initSettings](./settings.md#initsettings) and pass his own settings.

**Return Value**

A promise that resolves when the capturing process has successfully started. It does not provide any value upon resolution.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
await router.startCapturing("ReadSingleBarcode");
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
await router.startCapturing("ReadSingleBarcode");
// ...
router.stopCapturing();
```