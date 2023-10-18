---
layout: default-layout
title: interface FileImageTag - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface FileImageTag in Dynamsoft Core Module.
keywords: file image tag, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# FileImageTag

The interface FileImageTag represents an image tag that is associated with a file. It inherits from the ImageTag class and adds two attributes, a file path and a page number.

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
