---
layout: default-layout
title: interface FileImageTag - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface FileImageTag in Dynamsoft Core Module.
keywords: file image tag, JS
needAutoGenerateSidebar: true
---

# FileImageTag

The interface FileImageTag represents an image tag that is associated with a file. It inherits from the ImageTag class and adds two attributes, a file path and a page number.

## Definition

```js
export interface FileImageTag extends ImageTag {
                filePath: string;
                pageNumber: number;
            }
```

## Attributes Summary

| Attribute               | Type |
|----------------------|-------------|
| [`filePath`](#filePath) | *string* |
| [`pageNumber`](#pageNumber) | *number* |

### filePath

Gets the file path of the image tag.

```js
filePath: string;
```

### pageNumber

Gets the page number of the image tag.

```js
pageNumber: number;
```
