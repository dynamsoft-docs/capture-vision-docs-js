---
layout: default-layout
title: Class IdentityProcessor - Dynamsoft Barcode Reader JS Edition API Reference
description: This page shows the JS edition of the class IdentityProcessor in Dynamsoft Barcode Reader JS Edition.
keywords: IdentityProcessor, identity document, portrait zone, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# IdentityProcessor

The `IdentityProcessor` class provides utility APIs for processing identity documents.

| Name                                              | Description                                                             |
| ------------------------------------------------- | ----------------------------------------------------------------------- |
| `static` [findPortraitZone()](#findportraitzone)  | Finds the precise location of the portrait zone on an identity document. |

## findPortraitZone

Finds the precise location of the portrait zone on an identity document.

```typescript
static findPortraitZone(): Promise<Quadrilateral | null>;
```

**Return Value**

A promise that resolves with a `Quadrilateral` object defining the precise location of the portrait zone found in the image, or `null` if no portrait zone is detected.

**See also**

* [Quadrilateral]({{ site.dcvb_js_api }}core/basic-structures/quadrilateral.html)

**Code snippet**

```javascript
const quad = await Dynamsoft.DBR.IdentityProcessor.findPortraitZone();
if (quad) {
    console.log("Portrait zone found:", quad);
} else {
    console.log("No portrait zone detected.");
}
```

**Remarks**

New added in CaptureVisionBundle version 3.4.2000.