---
layout: default-layout
title: interface IntermediateResultUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface IntermediateResultUnit in Dynamsoft Core Module.
keywords: intermediate result, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResultUnit

The IntermediateResultUnit interface represents an intermediate result unit used in image processing.

## Definition

```typescript
interface IntermediateResultUnit {
                hashId: string;
                sourceImageHashId: string;
                sourceImageTag: Core.BasicStructures.ImageTag;
                localToSourceImageTransformMatrix: Array<{ local: number, source: number }>;
                unitType: EnumIntermediateResultUnitType;
            }
```


| API Name               | Description |
|----------------------|-------------|
| [`hashId`](#hashId) | Gets the hash ID of the unit.|
| [`sourceImageHashId`](#sourceImageHashId) | Gets the hash ID of the source image. |
| [`sourceImageTag`](#sourceImageTag) | Gets the image tag of the source image. |
| [`localToSourceImageTransformMatrix`](#localToSourceImageTransformMatrix) | Gets the transformation matrix from local to source image coordinates. |
| [`unitType`](#unitType) | Gets the type of the intermediate result unit. |

### hashId

The hash ID of the intermediate result unit.

```typescript
hashId: string;
```

**Return value**

Returns the hash ID of the unit. 

### sourceImageHashId

The hash ID of the source image.

```typescript
sourceImageHashId: string;
```

**Return value**

Returns the hash ID of the source image.

### sourceImageTag

The image tag of the source image.

```typescript
sourceImageTag: Core.BasicStructures.ImageTag;
```

**Return value**

Returns the image tag of the source image.

### localToSourceImageTransformMatrix

The transformation matrix from local to source image coordinates.

```typescript
virtual void GetLocalToSourceImageTransformMatrix(double matrix[9]) const
```

### unitType

The type of the intermediate result unit.

```typescript
unitType: EnumIntermediateResultUnitType;
```
