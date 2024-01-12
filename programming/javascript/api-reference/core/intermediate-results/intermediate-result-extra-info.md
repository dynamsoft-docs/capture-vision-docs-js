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

The `IntermediateResultExtraInfo` structure represents the extra information associated with an intermediate result. It includes properties such as the target ROI definition name, task name, section level result indicator, and section type.

```typescript
interface IntermediateResultExtraInfo {
    targetROIDefName: string;
    taskName: string;
    isSectionLevelResult: boolean;
    sectionType: EnumSectionType;
};
```

| Properties                                             | Type                                |
| ----------------------------------------------------- | ----------------------------------- |
| [targetROIDefName](#targetroidefname)               | *String*                            |
| [taskName](#taskname)                               | *String*                            |
| [isSectionLevelResult](#issectionlevelresult)       | *boolean*                           |
| [sectionType](#sectiontype)                         | *EnumSectionType*                   |

## targetROIDefName

Specifies the name of the TargetROIDef object that generates the intermediate result.

```typescript
targetROIDefName: string;
```

## taskName

Specifies the name of the task that generates the intermediate result.

```typescript
taskName: string;
```

## isSectionLevelResult

Specifies whether the intermediate result is a section-level result.

```typescript
isSectionLevelResult: boolean;
```

## sectionType

Specifies the SectionType that generates the intermediate result.

```typescript
sectionType: EnumSectionType;
```