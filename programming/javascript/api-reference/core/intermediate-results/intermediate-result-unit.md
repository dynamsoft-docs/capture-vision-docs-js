---
layout: default-layout
title: interface IntermediateResultUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface IntermediateResultUnit in Dynamsoft Core Module.
keywords: intermediate result, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# IntermediateResultUnit

The `IntermediateResultUnit` interface represents an intermediate result unit used in image processing.

## Definition

```typescript
interface IntermediateResultUnit {
    hashId: string;
    OriginalImageHashId: string;
    originalImageTag: Core.BasicStructures.ImageTag;
    unitType: EnumIntermediateResultUnitType;
    getTransformMatrix(matrixType: EnumTransformMatrixType): Array<number>
}
```

| API Name               | Description |
|----------------------|-------------|
| [hashId](#hashid) | Gets the hash ID of the unit.|
| [originalImageHashId](#originalimagehashid) | Gets the hash ID of the original image. |
| [originalImageTag](#originalimagetag) | Gets the image tag of the original image. |
| [unitType](#unittype) | Gets the type of the intermediate result unit. |
| [getTransformMatrix](#gettransformmatrix) | Gets the transformation matrix from local to original image coordinates. |

### hashId

The hash ID of the intermediate result unit.

```typescript
hashId: string;
```

**Return value**

Returns the hash ID of the unit. 

### originalImageHashId

The hash ID of the original image.

```typescript
OriginalImageHashId: string;
```

**Return value**

Returns the hash ID of the original image.

### originalImageTag

The image tag of the original image.

```typescript
originalImageTag: Core.BasicStructures.ImageTag;
```

**Return value**

Returns the image tag of the original image.

### unitType

The type of the intermediate result unit.

```typescript
unitType: EnumIntermediateResultUnitType;
```

### getTransformMatrix

Get the transformation matrix from local to original image coordinates.

```typescript
getTransformMatrix(matrixType: EnumTransformMatrixType): Array<number>;
```

**Parameter**

`matrixType`:A specific enumeration type to determine the type of transformation matrix to retrieve.

**Return value**

Return the matrix which is an Array of 9 numbers.