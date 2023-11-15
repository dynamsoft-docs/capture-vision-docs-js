---
layout: default-layout
title: Interface ImageSourceStateListener - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces interface related to the ImageSourceStateListener of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, router, Intermediate-result, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ImageSourceStateListener

The `ImageSourceStateListener` interface represents a listener for capture state changes. It defines a callback function `onImageSourceStateReceived` that will be called when the image source state changes.

## Definition

```typescript
interface ImageSourceStateListener {
  onImageSourceStateReceived?: (status: EnumImageSourceState) => void;
}
```

### onImageSourceStateReceived

```typescript
onImageSourceStateReceived?: (status: EnumImageSourceState) => void;
```

**Parameters**

`status`: The parameter status represents the received image source state. It is of type `EnumImageSourceState`, which is an enumeration representing different image source states.

**Return Value**

None.

**Code snippet**

```javascript
let issl = {
  onImageSourceStateListener(state) {
    console.log("Image Source State: ", state);
  }
}
```

**See Also**

* [EnumImageSourceState]({{ site.enums }}core/image-source-state.html?lang=js)