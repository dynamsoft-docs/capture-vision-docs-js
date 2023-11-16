---
layout: default-layout
title: interface FileImageTag - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface FileImageTag in Dynamsoft Core Module.
keywords: file image tag, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# FileImageTag

The `FileImageTag` interface defines a structure that contains extra information about an image that is loaded from a file. It inherits from the [`ImageTag`](./image-tag.md) interface with two added attributes: `filePath` and `pageNumber`.

## Definition

```typescript
interface FileImageTag extends ImageTag {
    filePath: string;
    pageNumber: number;
}
```

| Properties               | Type |
|----------------------|-------------|
| [`filePath`](#filepath) | *string* |
| [`pageNumber`](#pagenumber) | *number* |

### filePath

Gets the file path of the image tag.

```typescript
filePath: string;
```

### pageNumber

Gets the page number of the image tag.

```typescript
pageNumber: number;
```
