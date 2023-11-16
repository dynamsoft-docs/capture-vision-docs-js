---
layout: default-layout
title: interface IntermediateResultManager - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface IntermediateResultManager in Dynamsoft Core Module.
keywords: intermediate result manager, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# IntermediateResultManager

The `IntermediateResultManager` interface manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.

## Definition

```typescript
interface IntermediateResultManager {
    addResultReceiver(receiver: IntermediateResultReceiver): void;
    removeResultReceiver(receiver: IntermediateResultReceiver): void;
}
```

| API Name | Description |
|--------|-------------|
| [`addResultReceiver`](#addresultreceiver) | Adds an intermediate result receiver.|
| [`removeResultReceiver`](#removeresultreceiver) | Removes an intermediate result receiver. |

### addResultReceiver

Adds an intermediate result receiver to the manager.

```typescript
addResultReceiver(receiver: IntermediateResultReceiver): void;
```

**Parameters**

`receiver`: The intermediate result receiver to add.

### removeResultReceiver

Removes an intermediate result receiver from the manager.

```typescript
removeResultReceiver(receiver: IntermediateResultReceiver): void;
```

**Parameters**

`receiver`: The intermediate result receiver to remove.

<!--
### getOriginalImage

Gets the original image data using an image hash id.

```typescript
getOriginalImage(imageHashId: string): Promise<Core.BasicStructures.DSImageData>;
```

**Parameters**

`imageHashId`: The hash id of the image to retrieve.

**Return value**

Returns a promise to the DSImageData object containing the original image data.
-->