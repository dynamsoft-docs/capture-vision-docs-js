---
layout: default-layout
title: interface RegionObjectElement - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface RegionObjectElement in Dynamsoft Core Module.
keywords: region object element, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# RegionObjectElement

The RegionObjectElement interface represents an element of a region object in 2D space. It is an abstract interface that provides the interface for region object elements.

## Definition

```ts
export interface RegionObjectElement {
                location: Core.BasicStructures.Quadrilateral;
                referencedElement: RegionObjectElement;
                type: EnumRegionObjectElementType;
            }
```

## Attributes Summary

| Attribute               | Type |
|----------------------|-------------|
| [`location`](#location) | *Core.BasicStructures.Quadrilateral* |
| [`referencedElement`](#referencedelement) | *RegionObjectElement* |
| [`type`](#type) | *EnumRegionObjectElementType* |

### location

The location of the region object element.

```ts
location: Core.BasicStructures.Quadrilateral;
```

### referencedElement

A referenced region object element.

```ts
referencedElement: RegionObjectElement;
```

### type

Get the type of the region object element.

```ts
type: EnumRegionObjectElementType;
```