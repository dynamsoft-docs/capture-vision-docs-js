---
layout: default-layout
title: interface IntermediateResultManager - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface IntermediateResultManager in Dynamsoft Core Module.
keywords: intermediate result manager, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResultManager

The IntermediateResultManager interface manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get raw image data using an image hash id.

## Definition

```ts
export interface IntermediateResultManager {
                addResultReceiver: (receiver: IntermediateResultReceiver) => void;
                removeResultReceiver: (receiver: IntermediateResultReceiver) => void;
                getRawImage: (imageHashId: string) => Promise<Core.BasicStructures.DSImageData>;
            }
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`addResultReceiver`](#addresultreceiver) | Adds an intermediate result receiver.|
| [`removeResultReceiver`](#removeresultreceiver) | Removes an intermediate result receiver. |
| [`getRawImage`](#getrawimage) | Gets the raw image data using an image hash id. |

### addResultReceiver

Adds an intermediate result receiver to the manager.

```ts
addResultReceiver: (receiver: IntermediateResultReceiver) => void;
```

**Parameters**

`receiver` The intermediate result receiver to add.

### removeResultReceiver

Removes an intermediate result receiver from the manager.

```ts
removeResultReceiver: (receiver: IntermediateResultReceiver) => void;
```

**Parameters**

`receiver` The intermediate result receiver to remove.

### getRawImage

Gets the raw image data using an image hash id.

```ts
getRawImage: (imageHashId: string) => Promise<Core.BasicStructures.DSImageData>;
```

**Parameters**

`imageHashId` The hash id of the image to retrieve.

**Return value**

Returns a promise to the DSImageData object containing the raw image data.
