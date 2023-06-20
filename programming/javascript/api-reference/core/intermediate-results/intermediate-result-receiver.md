---
layout: default-layout
title: class CIntermediateResultReceiver - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CIntermediateResultReceiver in Dynamsoft Core Module.
keywords: intermediate result receiver, c++
needAutoGenerateSidebar: true
---

# CIntermediateResultReceiver

The CIntermediateResultReceiver class is responsible for receiving intermediate results of different types. It provides virtual functions for each type of result, which are called when the corresponding result is received.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CIntermediateResultReceiver 
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`GetObservedParameters`](#getobservedparameters) | Gets the types of intermediate result units that have been observed. |
| [`OnTaskResultsReceived`](#ontaskresultsreceived) | Called when a task result has been received. |
| [`OnPredetectedRegionsReceived`](#onpredetectedregionsreceived) | Called when predetected regions have been received. |
| [`OnLocalizedBarcodesReceived`](#onlocalizedbarcodesreceived) | Called when localized barcodes have been received. |
| [`OnDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | Called when decoded barcodes have been received. |
| [`OnLocalizedTextLinesReceived`](#onlocalizedtextlinesreceived) | Called when localized text lines have been received. |
| [`OnRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | Called when recognized text lines have been received. |
| [`OnDetectedQuadsReceived`](#ondetectedquadsreceived) | Called when detected quadrilaterals have been received. |
| [`OnNormalizedImagesReceived`](#onnormalizedimagesreceived) | Called when normalized images have been received. |
| [`OnColourImageUnitReceived`](#oncolourimageunitreceived) | Called when colour image units have been received. |
| [`OnScaledDownColourImageUnitReceived`](#onscaleddowncolourimageunitreceived) | Called when scaled down colour image units have been received. |
| [`OnGrayscaleImageUnitReceived`](#ongrayscaleimageunitreceived) | Called when grayscale image units have been received. |
| [`OnTransformedGrayscaleImageUnitReceived`](#ontransformedgrayscaleimageunitreceived) | Called when transformed grayscale image units have been received. |
| [`OnEnhancedGrayscaleImageUnitReceived`](#onenhancedgrayscaleimageunitreceived) | Called when enhanced grayscale image units have been received. |
| [`OnBinaryImageUnitReceived`](#onbinaryimageunitreceived) | Called when binary image units have been received. |
| [`OnTextureDetectionResultUnitReceived`](#ontexturedetectionresultunitreceived) | Called when texture detection result units have been received. |
| [`OnTextureRemovedGrayscaleImageUnitReceived`](#ontextureremovedgrayscaleimageunitreceived) | Called when texture removed grayscale image units have been received. |
| [`OnTextureRemovedBinaryImageUnitReceived`](#ontextureremovedbinaryimageunitreceived) | Called when texture removed binary image units have been received. |
| [`OnContoursUnitReceived`](#oncontoursunitreceived) | Called when contour units have been received. |
| [`OnLineSegmentsUnitReceived`](#onlinesegmentsunitreceived) | Called when line segment units have been received. |
| [`OnTextZonesUnitReceived`](#ontextzonesunitreceived) | Called when text zone units have been received. |
| [`OnTextRemovedBinaryImageUnitReceived`](#ontextremovedbinaryimageunitreceived) | Called when text removed binary image units have been received. |
| [`OnLongLinesUnitReceived`](#onlonglinesunitreceived) | Called when long line units have been received. |
| [`OnCornersUnitReceived`](#oncornersunitreceived) | Called when corner units have been received. |
| [`OnCandidateQuadEdgesUnitReceived`](#oncandidatequadedgesunitreceived) | Called when candidate quadrilateral edge units have been received. |
| [`OnCandidateBarcodeZonesUnitReceived`](#oncandidatebarcodezonesunitreceived) | Called when candidate barcode zone units have been received. |
| [`OnScaledUpBarcodeImageUnitReceived`](#onscaledupbarcodeimageunitreceived) | Called when scaled up barcode image units have been received. |
| [`OnDeformationResistedBarcodeImageUnitReceived`](#ondeformationresistedbarcodeimageunitreceived) | Called when deformation resisted barcode image units have been received. |
| [`OnComplementedBarcodeImageUnitReceived`](#oncomplementedbarcodeimageunitreceived) | Called when complemented barcode image units have been received. |

### GetObservedParameters

Gets the observed parameters of the intermediate result receiver.

```cpp
CObservedParameters* GetObservedParameters()
```

**Return value**

Returns the object of CObservedParameters. The default parameters are to observe all intermediate result unit types and all tasks.

### OnTaskResultsReceived

Called when a task result has been received.

```cpp
virtual void OnTaskResultsReceived(const CIntermediateResult *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the CIntermediateResult object that contains several result units.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnPredetectedRegionsReceived

Called when predetected regions have been received.

```cpp
virtual void OnPredetectedRegionsReceived(CPredetectedRegionsUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the CPredetectedRegionsUnit object that contains the result.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnLocalizedBarcodesReceived

Called when localized barcodes have been received.

```cpp
virtual void OnLocalizedBarcodesReceived(dbr::intermediate_results::CLocalizedBarcodesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the CLocalizedBarcodesUnit object that contains the result.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnDecodedBarcodesReceived

Called when decoded barcodes have been received.

```cpp
virtual void OnDecodedBarcodesReceived(dbr::intermediate_results::CDecodedBarcodesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the CDecodedBarcodesUnit object that contains the result.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnLocalizedTextLinesReceived

Called when localized text lines have been received.

```cpp
virtual void OnLocalizedTextLinesReceived(dlr::intermediate_results::CLocalizedTextLinesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the CLocalizedTextLinesUnit object that contains the result.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnRecognizedTextLinesReceived

Called when recognized text lines have been received.

```cpp
virtual void OnRecognizedTextLinesReceived(dlr::intermediate_results::CRecognizedTextLinesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the CRecognizedTextLinesUnit object that contains the result.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnDetectedQuadsReceived

Called when detected quadrilaterals have been received.

```cpp
virtual void OnDetectedQuadsReceived(ddn::intermediate_results::CDetectedQuadsUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the CDetectedQuadsUnit object that contains the result.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnNormalizedImagesReceived

Called when normalized images have been received.

```cpp
virtual void OnNormalizedImagesReceived(ddn::intermediate_results::CNormalizedImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the CNormalizedImageUnit object that contains the result.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnColourImageUnitReceived

Called when colour image units have been received.

```cpp
virtual void OnColourImageUnitReceived(CColourImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received colour image unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnScaledDownColourImageUnitReceived

Handles the receipt of a scaled-down colour image unit.

```cpp
virtual void OnScaledDownColourImageUnitReceived(CScaledDownColourImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received scaled-down colour image unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnGrayscaleImageUnitReceived

Handles the receipt of a grayscale image unit.

```cpp
virtual void OnGrayscaleImageUnitReceived(CGrayscaleImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received grayscale image unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnTransformedGrayscaleImageUnitReceived

Handles the receipt of a transformed grayscale image unit.

```cpp
virtual void OnTransformedGrayscaleImageUnitReceived(CTransformedGrayscaleImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received transformed grayscale image unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnEnhancedGrayscaleImageUnitReceived

Handles the receipt of an enhanced grayscale image unit.

```cpp
virtual void OnEnhancedGrayscaleImageUnitReceived(CEnhancedGrayscaleImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received enhanced grayscale image unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnBinaryImageUnitReceived

Handles the receipt of a binary image unit.

```cpp
virtual void OnBinaryImageUnitReceived(CBinaryImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received binary image unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnTextureDetectionResultUnitReceived

Handles the receipt of a texture detection result unit.

```cpp
virtual void OnTextureDetectionResultUnitReceived(CTextureDetectionResultUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received texture detection result unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnTextureRemovedGrayscaleImageUnitReceived

Handles the receipt of a texture-removed grayscale image unit.

```cpp
virtual void OnTextureRemovedGrayscaleImageUnitReceived(CTextureRemovedGrayscaleImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received texture-removed grayscale image unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnTextureRemovedBinaryImageUnitReceived

Handles the receipt of a texture-removed binary image unit.

```cpp
virtual void OnTextureRemovedBinaryImageUnitReceived(CTextureRemovedBinaryImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received texture-removed binary image unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnContoursUnitReceived

Handles the receipt of a contours unit.

```cpp
virtual void OnContoursUnitReceived(CContoursUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the contours unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnLineSegmentsUnitReceived

Called when a line segments unit is received.

```cpp
virtual void OnLineSegmentsUnitReceived(CLineSegmentsUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the line segments unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnTextZonesUnitReceived

Called when a text zones unit is received.

```cpp
virtual void OnTextZonesUnitReceived(CTextZonesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the text zones unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnTextRemovedBinaryImageUnitReceived

Called when a text removed binary image unit is received.

```cpp
virtual void OnTextRemovedBinaryImageUnitReceived(CTextRemovedBinaryImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the text removed binary image unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnLongLinesUnitReceived

Called when a long lines unit is received.

```cpp
virtual void OnLongLinesUnitReceived(ddn::intermediate_results::CLongLinesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the long lines unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnCornersUnitReceived

Called when a corners unit is received.

```cpp
virtual void OnCornersUnitReceived(ddn::intermediate_results::CCornersUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the corners unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnCandidateQuadEdgesUnitReceived

Called when a candidate quad edges unit is received.

```cpp
virtual void OnCandidateQuadEdgesUnitReceived(ddn::intermediate_results::CCandidateQuadEdgesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the candidate quad edges unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnCandidateBarcodeZonesUnitReceived

Called when a candidate barcode zones unit is received.

```cpp
virtual void OnCandidateBarcodeZonesUnitReceived(dbr::intermediate_results::CCandidateBarcodeZonesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the candidate barcode zones unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnScaledUpBarcodeImageUnitReceived

Called when a scaled up barcode image unit is received.

```cpp
virtual void OnScaledUpBarcodeImageUnitReceived(dbr::intermediate_results::CScaledUpBarcodeImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the scaled up barcode image unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnDeformationResistedBarcodeImageUnitReceived

Called when a deformation resisted barcode image unit is received.

```cpp
virtual void OnDeformationResistedBarcodeImageUnitReceived(dbr::intermediate_results::CDeformationResistedBarcodeImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the deformation resisted barcode image unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### OnComplementedBarcodeImageUnitReceived

Called when a complemented barcode image unit is received.

```cpp
virtual void OnComplementedBarcodeImageUnitReceived(dbr::intermediate_results::CComplementedBarcodeImageUnit *pResult，const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the complemented barcode image unit.

`[in] info` A pointer to the IntermediateResultExtraInfo object that contains the extra info of intermediate result.
