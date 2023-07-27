---
layout: default-layout
title: interface RawImageResultItem - Dynamsoft Capture Vision JS Edition API Reference
description: This page shows the JS edition of the interface RawImageResultItem in Dynamsoft Capture Vision Router Module.
keywords: raw image, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# RawImageResultItem

The `RawImageResultItem` interface represents a captured raw image result item. It extends the `CapturedResultItem` interface and adds a property.

## Definition

```typescript
interface RawImageResultItem extends CapturedResultItem {
                readonly imageData: Core.BasicStructures.DSImageData;
            }
```


| API Name                          | Description                                      |
| ------------------------------- | ------------------------------------------------ |
| [`imageData`](#imagedata) | Gets the image data for the RawImageResultItem. |

### imageData

`imageData`: A property of type `Core.BasicStructures.DSImageData` that represents the image data of the raw image result item.

```typescript
readonly imageData: Core.BasicStructures.DSImageData;
```