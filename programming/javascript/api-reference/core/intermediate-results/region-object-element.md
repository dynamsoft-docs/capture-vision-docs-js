---
layout: default-layout
title: Interface RegionObjectElement - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface RegionObjectElement in Dynamsoft Core Module.
keywords: region object element, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# RegionObjectElement

The `RegionObjectElement` interface represents a basic element of a region object, including its type, location and reference to another element.

```typescript
interface RegionObjectElement {
    elementType: EnumRegionObjectElementType;
    location: Quadrilateral;
    referencedElement: RegionObjectElement;
}
```

## elementType

The type of the region object element, defined by the enumeration `EnumRegionObjectElementType`.

**See Also**

[EnumRegionObjectElementType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/region-object-element-type.html?lang=js)        

## location

The location of the region object, represented as a quadrilateral.

**See Also**

[Quadrilateral](../basic-structures/quadrilateral.md)

## referencedElement

A reference to another `RegionObjectElement`.
