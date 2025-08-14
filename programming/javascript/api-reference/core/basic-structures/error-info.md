---
layout: default-layout
title: Interface ErrorInfo - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface ErrorInfo in Dynamsoft Core Module.
keywords: error info, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ErrorInfo

The `ErrorInfo` interface defines the structure for error objects returned by the `CaptureVisionRouter`.

```typescript
interface ErrorInfo {
    errorCode: EnumErrorCode;
    errorString: string
}
```

## errorCode

A predefined enumerated code that categorizes the type of error. This code is used programmatically to identify specific error conditions.

**See Also**
[EnumErrorCode]({{ site.dcvb_js_api }}enums-error-code.html?lang=js)

## errorString

A human-readable message that describes the error. This message can be displayed to users or logged for debugging purposes.
