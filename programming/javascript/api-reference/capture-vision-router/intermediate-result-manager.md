---
layout: default-layout
title: Class IntermediateResultManager - Dynamsoft CaptureVisionRouter Module JS Edition API Reference
description: This page introduces the IntermediateResultManager Class in Dynamsoft CaptureVisionRouter Module JS Edition.
keywords: IntermediateResultManager, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# IntermediateResultManager

The `IntermediateResultManager` class is responsible for handling intermediate results obtained during the process of an image. It offers methods to both register and deregister receivers of these intermediate results, as well as to retrieve the original image data.

| Name                                            | Description                                                                         |
| ----------------------------------------------- | ----------------------------------------------------------------------------------- |
| [addResultReceiver()](#addresultreceiver)       | Adds a `IntermediateResultReceiver` object as the receiver of intermediate results. |
| [removeResultReceiver()](#removeresultreceiver) | Removes the specified `IntermediateResultReceiver` object.                          |
| [removeAllResultReceivers()](#removeallresultreceivers) | Removes all `CapturedResultReceiver` objects.                             |
| [getOriginalImage()](#getoriginalimage)         | Retrieves the original image data.                                                  |

## addResultReceiver

Adds a `IntermediateResultReceiver` object as the receiver of intermediate results.

**Syntax**

```typescript
addResultReceiver(receiver: IntermediateResultReceiver): Promise<void>;
```

**Parameters**

`receiver`: the receiver object, of type `IntermediateResultReceiver`.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const intermediateResultReceiver = new Dynamsoft.CVR.IntermediateResultReceiver();
intermediateResultReceiver.onDecodedBarcodesReceived = (result, info) => {
    /* Do something with the result */
};
const intermediateResultManager = router.getIntermediateResultManager();
await intermediateResultManager.addResultReceiver(intermediateResultReceiver);
```

**See Also**

[IntermediateResultReceiver](../capture-vision-router/intermediate-result-receiver.md)

## removeResultReceiver

Removes the specified `IntermediateResultReceiver` object.

**Syntax**

```typescript
removeResultReceiver(receiver: IntermediateResultReceiver): Promise<void>;
```

**Parameters**

`receiver`: the receiver object, of type `IntermediateResultReceiver`.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const intermediateResultReceiver = new Dynamsoft.CVR.IntermediateResultReceiver();
intermediateResultReceiver.onDecodedBarcodesReceived = (result, info) => {
    /* Do something with the result */
};
const intermediateResultManager = router.getIntermediateResultManager();
await intermediateResultManager.addResultReceiver(intermediateResultReceiver);
// ...
await intermediateResultManager.removeResultReceiver(intermediateResultReceiver);
```

**See Also**

[IntermediateResultReceiver](../capture-vision-router/intermediate-result-receiver.md)

## removeAllResultReceivers

Removes all `CapturedResultReceiver` objects.

**Syntax**

```typescript
removeAllResultReceivers(): Promise<void>;
```

**Parameters**

None.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const receiver1 = new Dynamsoft.CVR.CapturedResultReceiver();
const receiver2 = new Dynamsoft.CVR.CapturedResultReceiver();
// ...
await router.addResultReceiver(receiver1);
await router.addResultReceiver(receiver2);
// ...
await router.removeAllResultReceivers();
```

**See also**

[CapturedResultReceiver](https://www.dynamsoft.com/capture-vision/docs/web/programming/javascript/api-reference/capture-vision-router/captured-result-receiver.html)

**Remarks**

New added in CaptureVisionBundle version 3.4.2000 & BarcodeReaderBundle version 11.4.2000.

### getOriginalImage

Retrieves the original image data.

```typescript
getOriginalImage(): DSImageData;
```

**Parameters**

None.

**Return value**

The original image on native resolution.

**See Also**

[DSImageData](../core/basic-structures/ds-image-data.md)