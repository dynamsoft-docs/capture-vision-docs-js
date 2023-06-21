---
layout: default-layout
title: struct IntermediateResultExtraInfo - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the struct IntermediateResultExtraInfo in Dynamsoft Core Module.
keywords: intermediate result, c++
needAutoGenerateSidebar: true
---

# IntermediateResultExtraInfo

The IntermediateResultExtraInfo structure represents the extra information for generating an intermediate result unit.

## Definition

*Assembly:* DynamsoftCore.dll

```cpp
typedef struct IntermediateResultExtraInfo
{
    const char* targetROIDefName;
    const char* taskName;
    bool isSectionLevelResult;
    SectionType sectionType;  
    char reserved[64];
}IntermediateResultExtraInfo;
```

## Attributes Summary

| Attribute                                             | Type                                |
| ----------------------------------------------------- | ----------------------------------- |
| [`targetROIDefName`](#targetroidefname)               | *const char\**                      |
| [`taskName`](#taskname)                               | *const char\**                      |
| [`isSectionLevelResult`](#issectionlevelresult)       | *bool*                              |
| [`sectionType`](#sectiontype)                         | *SectionType*                       |
| [`reserved`](#reserved)                               | *char[64]*                          |

### targetROIDefName

Specifies the name of the TargetROIDef object that generates the intermediate result.

```cpp
const char* targetROIDefName
```

### taskName

Specifies the name of the task that generates the intermediate result.

```cpp
const char* taskName
```

### isSectionLevelResult

Specifies whether the intermediate result is section-level result.

```cpp
bool isSectionLevelResult
```

### sectionType

Specifies the SectionType that generates the intermediate result.

```cpp
SectionType sectionType
```

### reserved

Reserved for future use.

```cpp
char reserved[64]
```
