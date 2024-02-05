---
layout: default-layout
title: Interface ImageSourceStateListener - Dynamsoft CaptureVisionRouter Module JS Edition API Reference v2.0.30
description: This page introduces the ImageSourceStateListener interface in Dynamsoft CaptureVisionRouter Module JS Edition v2.0.30.
keywords: capture vision, router, Intermediate-result, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ImageSourceStateListener

The `ImageSourceStateListener` interface provides a standardized way for monitoring changes in the state of an image source. Utilizing an event-driven design, it features the event `onImageSourceStateReceived`, which is triggered whenever there is a change in the image source's state.

```typescript
interface ImageSourceStateListener {
    onImageSourceStateReceived?: (state: EnumImageSourceState) => void;
}
```

## onImageSourceStateReceived

Event triggered whenever there is a change in the image source's state.

```typescript
onImageSourceStateReceived?: (state: EnumImageSourceState) => void;
```

**Parameters**

`state`: This parameter indicates the current state of the image source, using the `EnumImageSourceState` type. This enumeration defines various possible states of an image source.

**Return Value**

None.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let imageSourceStateListener = {
    onImageSourceStateReceived(state) {
        console.log("Image Source State: ", state);
    }
}
router.
```

**See Also**

* [EnumImageSourceState]({{ site.enums }}core/image-source-state.html?lang=js)