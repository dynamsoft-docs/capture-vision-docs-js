---
layout: default-layout
title: interface CapturedResult - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface CapturedResult in Dynamsoft Core Module.
keywords: captured result, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResult

The CapturedResult provides access to the source image information and the list of captured result items, allowing you to retrieve and process the captured data as needed.

## Definition

```typescript
interface CapturedResult {
                readonly OriginalImageHashId: string;
                readonly OriginalImageTag: ImageTag;
                readonly items: Array<CapturedResultItem>;
            }
```



| Properties            | Type |
|----------------------|-------------|
| [`OriginalImageHashId`](#originalimagehashid) | *String* |
| [`OriginalImageTag`](#originalimagetag) | *ImageTag* |
| [`items`](#items) | *Array* |

### OriginalImageHashId

A string representing the hash ID of the source image.

```typescript
readonly OriginalImageHashId: string;
```

### OriginalImageTag

An `ImageTag` object representing the tag associated with the source image.

```typescript
readonly OriginalImageTag: ImageTag;
```

### items

An array of `CapturedResultItem` objects representing the captured result items.

```typescript
readonly items: Array<CapturedResultItem>;
```