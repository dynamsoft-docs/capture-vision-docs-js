---
layout: default-layout
title: Interface ObservationParameters - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface ObservationParameters in Dynamsoft Core Module.
keywords: intermediate result, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ObservationParameters

The `ObservationParameters` interface is used to set filter conditions for the `IntermediateResultReceiver`, so that only intermediate results meeting specific conditions will be called back.

```typescript
interface ObservationParameters {
    getObservedResultUnitTypes(): BigInt;
    setObservedResultUnitTypes(types: BigInt): void;
    isResultUnitTypeObserved(type: EnumIntermediateResultUnitType): boolean;
    addObservedTask(taskName): void;
    removeObservedTask(taskName: string): void;
    isTaskObserved(ctaskName: string): boolean;
}
```
<!--
| Name              | Description |
|----------------------|-------------|
| [getObservedResultUnitTypes()](#getobservedresultunittypes) | Gets the types of intermediate result units that have been observed. |
| [setObservedResultUnitTypes()](#setobservedresultunittypes) | Sets the types of intermediate result units that have been observed.|
| [isResultUnitTypeObserved()](#isresultunittypeobserved) | Determines whether the specified result unit type was observed. |
| [addObservedTask()](#addobservedtask) | Adds observed task name to be notified when relevant results are available. |
| [removeObservedTask()](#removeobservedtask) | Remove the observed task name so that intermediate results generated by the task are not notified. |
| [isTaskObserved()](#istaskobserved) | Determines whether the specified task was observed. |
-->

## getObservedResultUnitTypes

Gets the types of intermediate result units that have been observed.

```typescript
getObservedResultUnitTypes(): BigInt;
```

**Return value**

The observed types of intermediate result units.

## setObservedResultUnitTypes

Sets the types of intermediate result units that have been observed.

```typescript
setObservedResultUnitTypes(types: BigInt): void;
```

**Parameters**

`types`: The observed types of intermediate result units.

## isResultUnitTypeObserved

Determines whether the specified result unit type was observed.

```typescript
isResultUnitTypeObserved(type: EnumIntermediateResultUnitType): boolean;
```

**Return value**

Returns a boolean value indicating whether the specified result unit type was observed.

## addObservedTask

Adds observed task name to be notified when relevant results are available.

```typescript
addObservedTask(taskName): void;
```

**Parameters**

`taskName`: The specified task name.

## removeObservedTask

Remove the observed task name so that intermediate results generated by the task are not notified.

```typescript
removeObservedTask(taskName: string): void;
```

**Parameters**

`taskName`: The specified task name.

## isTaskObserved

Determines whether the specified task was observed.

```typescript
isTaskObserved(taskName: string): boolean;
```

**Parameters**

`taskName`: The specified task name.

**Return value**

Returns a boolean value indicating whether the specified task was observed.
