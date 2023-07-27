---
layout: default-layout
title: interface MultiFrameResultCrossFilter - Dynamsoft Utility Module JS Edition API Reference
description: This page shows the JS edition of the class MultiFrameResultCrossFilter in Dynamsoft Utility Module.
keywords: image manager, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# MultiFrameResultCrossFilter

The MultiFrameResultCrossFilter interface provides APIs for filtering out results that meet specific requirements.

## Definition

```typescript
interface MultiFrameResultCrossFilter {
    enableResultVerification: (resultItemTypes: number, enabled: boolean) => void;
    isResultVerificationEnabled: (type: Core.BasicStructures.EnumCapturedResultItemType) => boolean;
    enableDuplicateFilter: (resultItemTypes: number, enabled: boolean) => void;
    isDuplicateFilterEnabled: (type: Core.BasicStructures.EnumCapturedResultItemType) => boolean;
    setDuplicateForgetTime: (resultItemTypes: number, time: number) => Promise<void>;
    getDuplicateForgetTime: (type: Core.BasicStructures.EnumCapturedResultItemType) => Promise<number>;
}
```


| API Name                                                      | Description                                                                                                                                             |
| ------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`enableResultVerification`](#enableresultverification)       | Enables result verification feature to improve the accuracy of video streaming recognition results.                                                     |
| [`isResultVerificationEnabled`](#isresultverificationenabled) | Determines whether the result verification feature is enabled for the specific captured result item type.                                               |
| [`enableDuplicateFilter`](#enableduplicatefilter)             | Enables duplicate filter feature to filter out the duplicate results in the period of duplicateForgetTime for video streaming recognition.              |
| [`isDuplicateFilterEnabled`](#isduplicatefilterenabled)       | Determines whether the duplicate filter feature is enabled for the specific result item type.                                                           |
| [`setDuplicateForgetTime`](#setduplicateforgettime)           | Sets the duplicate forget time for the specific captured result item types. The same captured result item will be returned only once during the period. |
| [`getDuplicateForgetTime`](#getduplicateforgettime)           | Gets the duplicate forget time for a specific captured result item type.                                                                                |


### enableResultVerification

A method that enables or disables result verification for specific result item types.

```typescript
enableResultVerification: (resultItemTypes: number, enabled: boolean) => void;
```

**Parameters**

`resultItemTypes`:  The or value of the captured result item types.
`enabled`: Set whether to enable result verification.

**Return Value**

None.

### isResultVerificationEnabled

A method that checks whether result verification is enabled for a specific result item type.

```typescript
isResultVerificationEnabled: (type: Core.BasicStructures.EnumCapturedResultItemType) => boolean;
```

**Parameters**

`type`:  Specifies the captured result item type..

**Return Value**

Returns a boolean value indicating whether result verification is enabled for the specific captured result item type.

### enableDuplicateFilter

A method that enables or disables duplicate filtering for specific result item types.

```typescript
enableDuplicateFilter: (resultItemTypes: number, enabled: boolean) => void;
```

**Parameters**

`resultItemTypes`:  The or value of the captured result item types.
`enabled`: Set whether to enable result verification.

**Return Value**

None.

### isDuplicateFilterEnabled

A method that checks whether duplicate filtering is enabled for a specific result item type.

```typescript
isDuplicateFilterEnabled: (type: Core.BasicStructures.EnumCapturedResultItemType) => boolean;
```

**Parameters**

`type`:  Specifies the captured result item type..

**Return Value**

Returns a boolean value indicating whether duplicate filter is enabled for the specific result item type.

### setDuplicateForgetTime

A method that sets the time duration after which duplicate results should be forgotten for specific result item types.

```typescript
setDuplicateForgetTime: (resultItemTypes: number, time: number) => Promise<void>;
```

**Parameters**

`resultItemTypes`: The or value of the captured result item types.
`time`: The duplicate forget time measured in milliseconds.

**Return Value**

Returns a Promise that resolves when this operation are complete.

### getDuplicateForgetTime

A method that retrieves the time duration after which duplicate results are forgotten for a specific result item type.

```typescript
getDuplicateForgetTime: (type: Core.BasicStructures.EnumCapturedResultItemType) => Promise<number>;
```

**Parameters**

`type`: Specifies the captured result item type..

**Return Value**

Returns the duplicate forget time for the specific captured result item type.
