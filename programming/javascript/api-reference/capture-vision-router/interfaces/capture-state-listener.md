---
layout: default-layout
title: Interface CaptureStateListener - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces interface related to the CaptureStateListener of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, router, Intermediate-result, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
---

# Javascript API Reference - CaptureStateListener

| API Name                                                      | Description                                               |
| ------------------------------------------------------------- | --------------------------------------------------------- |
| [onCaptureStateChanged()](#oncapturestatechanged)             | Called when the capture state changes.                    |

## onCaptureStateChanged

The `CaptureStateListener` interface represents a listener for capture state changes. It defines a callback function `onCaptureStateChanged` that will be called when the capture state changes.

**Syntax**

```ts
export interface CaptureStateListener {
            onCaptureStateChanged?: (state: EnumCaptureState) => void;
        }
```

**Parameters**

`state`: The parameter state represents the updated capture state. It is of type `EnumCaptureState`, which is an enumeration representing different capture states.

**Return Value**

None.

**Code Snippet**

```ts
let csl = {
      onCaptureStateChanged(state) {
        console.log("run CaptureStateListener", state);
      }
    }
```