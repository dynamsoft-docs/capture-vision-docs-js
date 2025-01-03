---
layout: default-layout
title: Interface CapturedResult - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface CapturedResult in Dynamsoft Core Module.
keywords: captured result, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/javascript/api-reference/core/basic-structures/captured-result-v3.0.10.html
---

# CapturedResult

The [CapturedResult]({{ site.dcv_js_api }}core/basic-structures/captured-result.html) interface describes the basic structure of a result item returned by Dynamsoft Capture Vision Router.

```typescript
interface CapturedResult {
    readonly originalImageHashId: string;
    readonly originalImageTag: ImageTag;
    readonly items: Array<CapturedResultItem>;
}
```

| Properties                                  | Type       |
| ------------------------------------------- | ---------- |
| [originalImageHashId](#originalimagehashid) | *String*   |
| [originalImageTag](#originalimagetag)       | *ImageTag* |
| [items](#items)                             | *Array*    |

## originalImageHashId

A string representing the hash ID of the original image.

```typescript
readonly originalImageHashId: string;
```

## originalImageTag

An `ImageTag` object representing the tag associated with the original image.

```typescript
readonly originalImageTag: ImageTag;
```

## items

An array of [CapturedResultItem](./captured-result-item.md) objects representing the captured result items.

```typescript
readonly items: Array<CapturedResultItem>;
```