---
layout: default-layout
title: DLR Module Release Notes - Dynamsoft Capture Vision JavaScript Edition
description: The release notes of DynamsoftLabelRecognizer module - Dynamsoft Capture Vision JavaScript Edition.
keywords: release notes, label recognizer, JavaScript, DLR
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftLabelRecognizer Module

## 3.2.30 (05/15/2024)

### Changed

- Updated the DLR algorithm to v3.2.30, see[DLR C++ v3.2.30](https://www.dynamsoft.com/capture-vision/docs/server/programming/cplusplus/release-notes/dlr.html#3230-05132024) for more details.
- Added new APIs for users to obtain the cached character items and the character clusters:
  - A new interface `BufferedCharacterItemSet` to represent a collection of buffered character items and cluster information.
  - A new interface `BufferedCharacterItem` to represent a basic item of the buffered characters with its image and features information.
  - A new interface `CharacterCluster` to represent a character cluster generated from the collected buffered character items.

## 3.0.30 (02/02/2024)

The first version of `DynamsoftLabelRecognizer (DLR)` JavaScript edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.

DLR algorithm based on v3.0.30, see[DLR C++ v2.0.30](https://www.dynamsoft.com/capture-vision/docs/server/programming/cplusplus/release-notes/dlr.html#3030-02012024) for more details.