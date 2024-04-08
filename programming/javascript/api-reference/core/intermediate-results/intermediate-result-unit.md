---
layout: default-layout
title: Interface IntermediateResultUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface IntermediateResultUnit in Dynamsoft Core Module.
keywords: intermediate result, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# IntermediateResultUnit

The `IntermediateResultUnit` interface represents the base structure for units of intermediate results in image processing. This interface acts as a base and contains common properties and methods shared by all intermediate result units.

```typescript
interface IntermediateResultUnit {
    hashId: string;
    originalImageHashId: string;
    originalImageTag: Core.ImageTag;
    unitType: EnumIntermediateResultUnitType;
}
```

<!-- 
    getTransformMatrix(matrixType: EnumTransformMatrixType): Array<number>
    -->

## hashId

A unique identifier for the intermediate result unit.

## originalImageHashId

The hash ID of the original image associated with this unit.

## originalImageTag

The tag associated with the original image.

## unitType

The type of the intermediate result unit, defined by the enumeration `EnumIntermediateResultUnitType`.

**See Also**

[EnumIntermediateResultUnitType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/intermediate-result-unit-type.html?lang=js)

<!-- ## getTransformMatrix

Gets the transformation matrix associated with the unit, based on the specified matrix type.

```typescript
getTransformMatrix(matrixType: EnumTransformMatrixType): Array<number>;
```

**Parameter**

`matrixType`: The type of transformation matrix to retrieve.

**Return value**

An array of 9 numbers representing the transformation matrix.

**See Also**

[EnumTransformMatrixType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/transform-matrix-type.html?lang=js) -->
