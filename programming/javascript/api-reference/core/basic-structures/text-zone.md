---
layout: default-layout
title: Interface TextZone - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface TextZone in Dynamsoft Core Module.
keywords: image tag, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# TextZone

The `TextZone` interface describes a text zone.

```typescript
interface TextZone {
    location: Quadrilateral;
    charContoursIndices: Array<number>;
}
```

## location

The location of the text zone.

[Quadrilateral](./quadrilateral.md)

## charContoursIndices

The indices of the character contours.
