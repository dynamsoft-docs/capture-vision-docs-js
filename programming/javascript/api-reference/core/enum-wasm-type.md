---
layout: default-layout
title: EnumWasmType - Dynamsoft Core Enumerations
description: The enumeration EnumWasmType of Dynamsoft Core describes the types of WebAssembly (.wasm) builds that can be loaded.
keywords: WASM type, wasm, WebAssembly, EnumWasmType
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: EnumWasmType
codeAutoHeight: true
---

# Enumeration EnumWasmType

`EnumWasmType` describes the types of WebAssembly (.wasm) builds that can be loaded by the SDK. It is used as the value of the `wasmType` property of [wasmLoadOptions](./core-module-class.md#wasmloadoptions).

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumWasmType {
    /** Baseline build. Does not include ML, SIMD, pthread, or PDF support. */
    BASELINE = "baseline",
    /** Build with ML (neural network) support. */
    ML = "ml",
    /** Build with ML and SIMD support. */
    ML_SIMD = "ml-simd",
    /** Build with ML, SIMD, and pthread (multi-threading) support. */
    ML_SIMD_PTHREAD = "ml-simd-pthread",
    /** Build with ML, SIMD, and PDF reading support. */
    ML_SIMD_WITH_PDF = "ml-simd-with-pdf",
    /** Build with ML, SIMD, pthread (multi-threading), and PDF reading support. */
    ML_SIMD_PTHREAD_WITH_PDF = "ml-simd-pthread-with-pdf",
    /** The SDK selects the build automatically based on the runtime environment. */
    AUTO = "auto"
}
```

**Remarks**

Builds with pthread (multi-threading) support, such as `ml-simd-pthread` and `ml-simd-pthread-with-pdf`, require a cross-origin isolated page (for example, the page is served with the `Cross-Origin-Opener-Policy` and `Cross-Origin-Embedder-Policy` headers), because they depend on `SharedArrayBuffer`.
