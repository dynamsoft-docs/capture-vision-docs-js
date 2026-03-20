---
layout: default-layout
title: Interface AuxiliaryRegionElement - Dynamsoft Capture Vision JS Edition API Reference
description: The interface AuxiliaryRegionElement of Dynamsoft Capture Vision JS edition represents an auxiliary region element with a name and confidence level.
keywords: Auxiliary region element
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: AuxiliaryRegionElement
---

# AuxiliaryRegionElement

The `AuxiliaryRegionElement` interface represents an auxiliary region element detected within an image, such as a portrait zone or signature area. It extends `RegionObjectElement` with a name and confidence level.

```typescript
interface AuxiliaryRegionElement extends RegionObjectElement {
    name: string;
    confidence: number;
}
```

| Property                    | Description                                              |
| --------------------------- | -------------------------------------------------------- |
| [name](#name)               | The name of the auxiliary region.                        |
| [confidence](#confidence)   | The confidence level of the auxiliary region detection.  |

## name

The name identifying the type of this auxiliary region (e.g., `"PortraitZone"`, `"SignatureArea"`).

```typescript
name: string;
```

## confidence

The confidence level of this auxiliary region detection, typically in the range [0, 100].

```typescript
confidence: number;
```

**See Also**

* [RegionObjectElement](./region-object-element.html)
