---
layout: default-layout
title: Interface IntermediateResultExtraInfo - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface IntermediateResultExtraInfo in Dynamsoft Core Module.
keywords: intermediate result, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# IntermediateResultExtraInfo

The `IntermediateResultExtraInfo` interface represents the extra information associated with an intermediate result. It includes properties such as the target ROI definition name, task name, section level result indicator, and section type.

```typescript
interface IntermediateResultExtraInfo {
    isSectionLevelResult: boolean;
    sectionType: EnumSectionType;
    targetROIDefName: string;
    taskName: string;
};
```

## isSectionLevelResult

Indicates whether the result is at the section level.

## sectionType

The type of section, if applicable, as defined by an enumeration.

**See Also**

[EnumSectionType]({{ site.dcvb_js_api }}enums-section-type.html?lang=js)

## targetROIDefName

The name of the target Region Of Interest (ROI) definition.

## taskName

The name of the processing task to which this result belongs.
