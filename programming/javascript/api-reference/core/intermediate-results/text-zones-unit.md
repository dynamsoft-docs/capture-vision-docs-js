---
layout: default-layout
title: interface TextZonesUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface TextZonesUnit in Dynamsoft Core Module.
keywords: text zones, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextZonesUnit

The `TextZonesUnit` interface represents a unit that contains text zones.

## Definition

```typescript
interface TextZonesUnit extends IntermediateResultUnit {
    textZones: Array<Core.BasicStructures.Quadrilateral>;
}
```

| Properties               | Type |
|----------------------|-------------|
| [`textZones`](#textzones) | *Array<Core.BasicStructures.Quadrilateral>* |

### textZones

An array of Quadrilateral objects representing the text zones in the unit.

```typescript
textZones: Array<Core.BasicStructures.Quadrilateral>;
```
