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
    enableResultCrossVerification(resultItemTypes: number, enabled: boolean): void;
    isResultCrossVerificationEnabled(type: Core.BasicStructures.EnumCapturedResultItemType): boolean;
    enableResultDeduplication(resultItemTypes: number, enabled: boolean): void;
    isResultDeduplicationEnabled(type: Core.BasicStructures.EnumCapturedResultItemType): boolean;
    setDuplicateForgetTime(resultItemTypes: number, time: number): Promise<void>;
    getDuplicateForgetTime(type: Core.BasicStructures.EnumCapturedResultItemType): Promise<number>;
}
```


| API Name                                                      | Description                                                                                                                                             |
| ------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`enableResultCrossVerification()`](#enableresultcrossverification)       | Enables result verification feature to improve the accuracy of video streaming recognition results.                                                     |
| [`isResultCrossVerificationEnabled()`](#isresultcrossverificationenabled) | Determines whether the result verification feature is enabled for the specific captured result item type.                                               |
| [`enableResultDeduplication()`](#enableresultdeduplication)             | Enables duplicate filter feature to filter out the duplicate results in the period of duplicateForgetTime for video streaming recognition.              |
| [`isResultDeduplicationEnabled()`](#isresultdeduplicationenabled)       | Determines whether the duplicate filter feature is enabled for the specific result item type.                                                           |
| [`setDuplicateForgetTime()`](#setduplicateforgettime)           | Sets the duplicate forget time for the specific captured result item types. The same captured result item will be returned only once during the period. |
| [`getDuplicateForgetTime()`](#getduplicateforgettime)           | Gets the duplicate forget time for a specific captured result item type.                                                                                |


### enableResultCrossVerification

A method that enables or disables result verification for specific result item types.

```typescript
enableResultCrossVerification(resultItemTypes: number, enabled: boolean): void;
```

**Parameters**

`resultItemTypes`:  The value of the captured result item types.
`enabled`: Set whether to enable result verification.

**Return Value**

None.

### isResultCrossVerificationEnabled

A method that checks whether result verification is enabled for a specific result item type.

```typescript
isResultCrossVerificationEnabled(type: Core.BasicStructures.EnumCapturedResultItemType): boolean;
```

**Parameters**

`type`:  Specifies the captured result item type..

**Return Value**

Returns a boolean value indicating whether result verification is enabled for the specific captured result item type.

### enableResultDeduplication

A method that enables or disables duplicate filtering for specific result item types.

```typescript
enableResultDeduplication(resultItemTypes: number, enabled: boolean): void;
```

**Parameters**

`resultItemTypes`:  The or value of the captured result item types.
`enabled`: Set whether to enable result verification.

**Return Value**

None.

### isResultDeduplicationEnabled

A method that checks whether duplicate filtering is enabled for a specific result item type.

```typescript
isResultDeduplicationEnabled(type: Core.BasicStructures.EnumCapturedResultItemType): boolean;
```

**Parameters**

`type`:  Specifies the captured result item type..

**Return Value**

Returns a boolean value indicating whether duplicate filter is enabled for the specific result item type.

### setDuplicateForgetTime

A method that sets the time duration after which duplicate results should be forgotten for specific result item types.

```typescript
setDuplicateForgetTime(resultItemTypes: number, time: number): Promise<void>;
```

**Parameters**

`resultItemTypes`: The or value of the captured result item types.
`time`: The duplicate forget time measured in milliseconds.

**Return Value**

Returns a Promise that resolves when this operation are complete.

### getDuplicateForgetTime

A method that retrieves the time duration after which duplicate results are forgotten for a specific result item type.

```typescript
getDuplicateForgetTime(type: Core.BasicStructures.EnumCapturedResultItemType): Promise<number>;
```

**Parameters**

`type`: Specifies the captured result item type..

**Return Value**

Returns the duplicate forget time for the specific captured result item type.
