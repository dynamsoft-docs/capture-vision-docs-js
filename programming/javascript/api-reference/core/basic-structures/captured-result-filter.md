---
layout: default-layout
title: class CCaptureResultFilter - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CCaptureResultFilter in Core Module.
keywords: captured result receiver, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: C++ CCaptureResultFilter Class
permalink: /programming/cplusplus/api-reference/core/basic-structures/captured-result-filter.html
---

# CCaptureResultFilter

The `CCaptureResultFilter` class is responsible for filtering captured results. It contains several callback functions for different types of results, including raw image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore.dll

```cpp
class CCaptureResultFilter 
```

## Methods Summary

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`CCaptureResultFilter`](#ccaptureresultfilter)               | Constructor                                          |
| [`~CCaptureResultFilter`](#ccaptureresultfilter)              | Destructor                                           |
| [`GetFilteredResultItemTypes`](#getfilteredresultitemtypes)       | Gets the types of observed result items.             |
| [`OnCapturedResultReceived`](#oncapturedresultreceived)           | Callback function for all captured results.          |
| [`OnRawImageResultReceived`](#onrawimageresultreceived)           | Callback function for raw image results.             |
| [`OnDecodedBarcodesReceived`](#ondecodedbarcodesreceived)         | Callback function for decoded barcodes results.      |
| [`OnRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | Callback function for recognized text lines results. |
| [`OnDetectedQuadsReceived`](#ondetectedquadsreceived)             | Callback function for detected quads results.        |
| [`OnNormalizedImagesReceived`](#onnormalizedimagesreceived)       | Callback function for normalized images results.     |
| [`OnParsedResultsReceived`](#onparsedresultsreceived)             | Callback function for parsed results.                |
| [`GetName`](#getname)       | Gets the name of the captured result filter.                                             |
| [`SetName`](#setname)       | Sets the name of the captured result filter.                                             |

### CCaptureResultFilter

Constructor.

```cpp
CCaptureResultFilter()
```

### ~CCaptureResultFilter

Destructor.

```cpp
virtual ~CCaptureResultFilter()
```

### GetFilteredResultItemTypes

Gets the types of filtered result items.

```cpp
unsigned int GetFilteredResultItemTypes()
```

**Return value**

Returns the types of filtered result items.

### OnCapturedResultReceived

Callback function for all captured results. It will be called once for each captured result.

```cpp
virtual void OnCapturedResultReceived(CCapturedResult* pResult)
```

**Parameters**

`[in] pResult` The captured result.

### OnRawImageResultReceived

Callback function for raw image results. It will be called once for each raw image result.

```cpp
virtual void OnRawImageResultReceived(CRawImageResultItem* pResult)
```

**Parameters**

`[in] pResult` The raw image result.

### OnDecodedBarcodesReceived

Callback function for decoded barcodes results. It will be called once for each decoded barcodes result.

```cpp
virtual void OnDecodedBarcodesReceived(dbr::CDecodedBarcodesResult* pResult)
```

**Parameters**

`[in] pResult` The decoded barcodes result.

### OnRecognizedTextLinesReceived

Callback function for recognized text lines results. It will be called once for each recognized text lines result.

```cpp
virtual void OnRecognizedTextLinesReceived(dlr::CRecognizedTextLinesResult* pResult)
```

**Parameters**

`[in] pResult` The recognized text lines result.

### OnDetectedQuadsReceived

Callback function for detected quads results. It will be called once for each detected quads result.

```cpp
virtual void OnDetectedQuadsReceived(ddn::CDetectedQuadsResult* pResult)
```

**Parameters**

`[in] pResult` The detected quads result.

### OnNormalizedImagesReceived

Callback function for normalized images results. It will be called once for each normalized images result.

```cpp
virtual void OnNormalizedImagesReceived(ddn::CNormalizedImagesResult* pResult)
```

**Parameters**

`[in] pResult` The normalized images result.

### OnParsedResultsReceived

Callback function for parsed results. It will be called once for each parsed result.

```cpp
virtual void OnParsedResultsReceived(dcp::CParsedResult* pResult)
```

**Parameters**

`[in] pResult` The parsed result.

### GetName

Gets the name of the captured result filter.  

```cpp
const char* GetName() const
```

**Return value**

Returns the name of the captured result filter.  

### SetName

Sets the name of the captured result filter.  

```cpp
void SetName(const char* name)
```

**Parameters**

`[in] name` The name of the captured result filter.
