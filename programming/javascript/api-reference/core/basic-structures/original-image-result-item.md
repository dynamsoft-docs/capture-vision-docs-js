---
layout: default-layout
title: interface OriginalImageResultItem - Dynamsoft Capture Vision JS Edition API Reference
description: This page shows the JS edition of the interface OriginalImageResultItem in Dynamsoft Capture Vision Router Module.
keywords: original image, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# OriginalImageResultItem

The `OriginalImageResultItem` interface represents original image result item. It extends the `CapturedResultItem` interface and adds a property.

## Definition

```typescript
interface OriginalImageResultItem extends CapturedResultItem {
                readonly imageData: Core.BasicStructures.DSImageData;
            }
```


| API Name                          | Description                                      |
| ------------------------------- | ------------------------------------------------ |
| [`imageData`](#imagedata) | Gets the image data for the OriginalImageResultItem. |

### imageData

`imageData`: A property of type `Core.BasicStructures.DSImageData` that represents the image data of the original image result item.

```typescript
readonly imageData: Core.BasicStructures.DSImageData;
```