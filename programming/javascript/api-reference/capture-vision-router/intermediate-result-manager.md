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
| [getOriginalImage()](#getoriginalimage)         | Retrieves the original image data.                                                  |

## addResultReceiver

Adds a `IntermediateResultReceiver` object as the receiver of intermediate results.

**Syntax**

```typescript
addResultReceiver(receiver: IntermediateResultReceiver): void;
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
intermediateResultManager.addResultReceiver(intermediateResultReceiver);
```

**See Also**

[IntermediateResultReceiver](../capture-vision-router/intermediate-result-receiver.md)

## removeResultReceiver

Removes the specified `IntermediateResultReceiver` object.

**Syntax**

```typescript
removeResultReceiver(receiver: IntermediateResultReceiver): void;
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
intermediateResultManager.addResultReceiver(intermediateResultReceiver);
// ...
intermediateResultManager.removeResultReceiver(intermediateResultReceiver);
```

**See Also**

[IntermediateResultReceiver](../capture-vision-router/intermediate-result-receiver.md)

### getOriginalImage

Retrieves the original image data.

```typescript
getOriginalImage(): Promise<DSImageData>;
```

**Parameters**

None.

**Return value**

A promise that resolves when the operation has successfully completed. It provides the original image upon resolution.

**See Also**

[DSImageData](../core/basic-structures/ds-image-data.md)