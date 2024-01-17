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

The [CapturedResult]({{ site.dcv_js_api }}core/basic-structures/captured-result.html) interface describes the basic structure of a result item returned by Dynamsoft Capture Vision Router.

> NOTE: 
> 
> Depending on the functional module that generated the result item, the interface may vary:
> 
> * dynamsoft-barcode-reader: DecodedBarcodesResult
> * dynamsoft-label-recognizer: RecognizedTextLinesResult
> * dynamsoft-document-normalizer: [DetectedQuadsResult](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/detected-quads-result.html) or [NormalizedImagesResult](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/normalized-images-result.html)
> * dynamsoft-code-parser: ParsedResult

```typescript
interface CapturedResult {
    readonly OriginalImageHashId: string;
    readonly OriginalImageTag: ImageTag;
    readonly items: Array<CapturedResultItem>;
    readonly errorCode: number;
    readonly errorString: string;
}
```

| Properties                                  | Type                         |
| ------------------------------------------- | ---------------------------- |
| [OriginalImageHashId](#originalimagehashid) | *String*                     |
| [OriginalImageTag](#originalimagetag)       | *ImageTag*                   |
| [items](#items)                             | *Array\<CapturedResultItem>* |
| [errorCode](#errorcode)                     | *number*                     |
| [errorString](#errorstring)                 | *string*                     |

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

An array of [CapturedResultItem](./captured-result-item.md) objects representing the captured result items.

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