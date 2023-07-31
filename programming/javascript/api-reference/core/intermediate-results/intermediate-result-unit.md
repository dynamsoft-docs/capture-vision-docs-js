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
                OriginalImageHashId: string;
                originalImageTag: Core.BasicStructures.ImageTag;
                ImageTransformMatrix: Array<{ local: number, source: number }>;
                unitType: EnumIntermediateResultUnitType;
            }
```


| API Name               | Description |
|----------------------|-------------|
| [`hashId`](#hashid) | Gets the hash ID of the unit.|
| [`originalImageHashId`](#originalimagehashid) | Gets the hash ID of the source image. |
| [`originalImageTag`](#originalimagetag) | Gets the image tag of the source image. |
| [`ImageTransformMatrix`](#imagetransformmatrix) | Gets the transformation matrix from local to source image coordinates. |
| [`unitType`](#unittype) | Gets the type of the intermediate result unit. |

### hashId

The hash ID of the intermediate result unit.

```typescript
hashId: string;
```

**Return value**

Returns the hash ID of the unit. 

### originalImageHashId

The hash ID of the source image.

```typescript
OriginalImageHashId: string;
```

**Return value**

Returns the hash ID of the source image.

### originalImageTag

The image tag of the source image.

```typescript
originalImageTag: Core.BasicStructures.ImageTag;
```

**Return value**

Returns the image tag of the source image.

### ImageTransformMatrix

The transformation matrix from local to source image coordinates.

```typescript
ImageTransformMatrix: Array<{ local: number, source: number }>;
```

### unitType

The type of the intermediate result unit.

```typescript
unitType: EnumIntermediateResultUnitType;
```
