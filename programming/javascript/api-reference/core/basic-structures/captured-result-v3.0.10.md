---
layout: default-layout
title: Interface CapturedResult - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface CapturedResult in Dynamsoft Core Module.
keywords: captured result, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/javascript/api-reference/core/basic-structures/captured-result-v2.0.10.html
---

# CapturedResult

The `CapturedResult` interface describes the basic structure of a result item returned by Dynamsoft Capture Vision Router.

```typescript
interface CapturedResult {
    readonly OriginalImageHashId: string;
    readonly OriginalImageTag: ImageTag;
    readonly items: Array<CapturedResultItem>;
}
```

| Properties            | Type |
|----------------------|-------------|
| [OriginalImageHashId](#originalimagehashid) | *String* |
| [OriginalImageTag](#originalimagetag) | *ImageTag* |
| [items](#items) | *Array* |

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