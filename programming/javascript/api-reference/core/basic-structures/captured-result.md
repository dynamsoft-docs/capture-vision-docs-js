---
layout: default-layout
title: Interface CapturedResult - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface CapturedResult in Dynamsoft Core Module.
keywords: captured result, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# CapturedResult

The `CapturedResult` interface describes the basic structure of a result item returned by Dynamsoft Capture Vision Router.

```typescript
interface CapturedResult {
    readonly OriginalImageHashId: string;
    readonly OriginalImageTag: ImageTag;
    readonly items: Array<CapturedResultItem>;
    readonly errorCode: number;
    readonly errorString: string;
}
```

| Properties            | Type |
|----------------------|-------------|
| [OriginalImageHashId](#originalimagehashid) | *String* |
| [OriginalImageTag](#originalimagetag) | *ImageTag* |
| [items](#items) | *Array\<CapturedResultItem>* |
| [errorCode](#errorcode) | *number* |
| [errorString](#errorstring) | *string* |

## OriginalImageHashId

A string representing the hash ID of the original image.

```typescript
readonly OriginalImageHashId: string;
```

## OriginalImageTag

An `ImageTag` object representing the tag associated with the original image.

```typescript
readonly OriginalImageTag: ImageTag;
```

## items

An array of `CapturedResultItem` objects representing the captured result items.

```typescript
readonly items: Array<CapturedResultItem>;
```

## errorCode

The error code of the capture operation.

```typescript
readonly errorCode: number;
```

## errorString

The error message of the capture operation.

```typescript
readonly errorString: string;
```