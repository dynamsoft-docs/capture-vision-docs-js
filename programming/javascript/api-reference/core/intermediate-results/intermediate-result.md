---
layout: default-layout
title: Interface IntermediateResult - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface IntermediateResult in Dynamsoft Core Module.
keywords: task results, intermediate results, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# IntermediateResult

The `IntermediateResult` interface represents the collection of all intermediate result units produced during image processing.

```typescript
interface IntermediateResult {
    intermediateResultUnits: Array<IntermediateResultUnit>;
}
```

## intermediateResultUnits

An array of `IntermediateResultUnit` objects, each representing a different type of intermediate result.

**See Also**

[IntermediateResultUnit](./intermediate-result-unit.md)