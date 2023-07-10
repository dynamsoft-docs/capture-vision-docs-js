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

```ts
export interface CapturedResult {
                readonly sourceImageHashId: string;
                readonly sourceImageTag: ImageTag;
                readonly items: Array<CapturedResultItem>;
            }
```

## Attributes Summary

| Attribute            | Type |
|----------------------|-------------|
| [`sourceImageHashId`](#sourceImageHashId) | *String* |
| [`sourceImageTag`](#sourceImageTag) | *ImageTag* |
| [`items`](#items) | *Array* |

### sourceImageHashId

A string representing the hash ID of the source image.

```ts
readonly sourceImageHashId: string;
```

### sourceImageTag

An `ImageTag` object representing the tag associated with the source image.

```ts
readonly sourceImageTag: ImageTag;
```

### items

An array of `CapturedResultItem` objects representing the captured result items.

```ts
readonly items: Array<CapturedResultItem>;
```