---
layout: default-layout
title: interface DSFile - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface DSFile in Dynamsoft Core Module.
keywords: DSFile, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSFile

The DSFile interface extends the File interface in JavaScript and provides an additional download method for downloading a file in memory to the local drive via the browser.

## Definition

```typescript
interface DSFile extends File {
                download: () => void;
            }
```

## Methods Summary

### download

Downloading a file in memory to the local drive via the browser.

```typescript
download: () => void;
```