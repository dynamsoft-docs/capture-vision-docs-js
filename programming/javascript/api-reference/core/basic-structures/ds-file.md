---
layout: default-layout
title: Interface DSFile - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface DSFile in Dynamsoft Core Module.
keywords: DSFile, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# DSFile

The `DSFile` interface extends the [File](https://developer.mozilla.org/en-US/docs/Web/API/File) interface and provides an additional download method for downloading a file in memory to the local drive via the browser.

```typescript
interface DSFile extends File {
    download(): void;
}
```

## download

Downloading a file in memory to the local drive via the browser.

```typescript
download(): void;
```