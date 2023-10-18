---
layout: default-layout
title: interface PredetectedRegionsUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface PredetectedRegionsUnit in Dynamsoft Core Module.
keywords: predetected regions, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# PredetectedRegionsUnit

The `PredetectedRegionsUnit` interface represents a unit that contains a collection of pre-detected regions. It inherits from the IntermediateResultUnit interface and stores the result of pre-detected regions.

## Definition

```typescript
interface PredetectedRegionsUnit extends IntermediateResultUnit {
    predetectedRegions: Array<PredetectedRegionElement>;
}
```

| Properties | Type |
|--------|-------------|
| [`predetectedRegions`](#predetectedregions) | *Array<PredetectedRegionElement>* |


### predetectedRegions

 An array of PredetectedRegionElement objects representing the predetected regions contained in the unit.

```typescript
predetectedRegions: Array<PredetectedRegionElement>;
```