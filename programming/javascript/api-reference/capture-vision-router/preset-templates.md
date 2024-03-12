---
layout: default-layout
title: Preset CaptureVisionTemplates - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces the Preset CaptureVisionTemplates
keywords: CaptureVisionTemplates, router, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
---

# Preset CaptureVisionTemplates

The following shows the preset CaptureVisionTemplates

| Template Name                           | Function Description                                                             | Available with                 |
| --------------------------------------- | -------------------------------------------------------------------------------- | ------------------------------ |
| **ReadBarcodes_Default**                | Scans a single barcode.                                                          | dynamsoft-barcode-reader       |
| **ReadSingleBarcode**                   | Quickly scans a single barcode.                                                  | dynamsoft-barcode-reader       |
| **ReadBarcodes_SpeedFirst**             | Prioritizes speed in scanning multiple barcodes.                                 | dynamsoft-barcode-reader       |
| **ReadBarcodes_ReadRateFirst**          | Maximizes the number of barcodes read.                                           | dynamsoft-barcode-reader       |
| **ReadBarcodes_Balance**                | Balances speed and quantity in reading multiple barcodes.                        | dynamsoft-barcode-reader       |
| **ReadDenseBarcodes**                   | Specialized in reading barcodes with high information density.                   | dynamsoft-barcode-reader       |
| **ReadDistantBarcodes**                 | Capable of reading barcodes from extended distances.                             | dynamsoft-barcode-reader       |
| **DetectDocumentBoundaries_Default**    | Identifies the edges of a document.                                              | dynamsoft-document-normalizer  |
| **NormalizeDocument_Default**           | Adjusts a document to a standard format using detected borders.                  | dynamsoft-document-normalizer  |
| **DetectAndNormalizeDocument_Default**  | Detects document edges and standardizes its format.                              | dynamsoft-document-normalizer  |
| **RecognizeTextLines_Default**          | Identifies and reads any text present.                                           | dynamsoft-label-recognizer     |
| **RecognizeNumbers**                    | Specializes in recognizing numerical data.                                       | dynamsoft-label-recognizer     |
| **RecognizeLetters**                    | Identifies both uppercase and lowercase English alphabets.                       | dynamsoft-label-recognizer     |
| **RecognizeNumbersAndLetters**          | Reads both numbers and English alphabets (any case).                             | dynamsoft-label-recognizer     |
| **RecognizeNumbersAndUppercaseLetters** | Scans numbers and uppercase English alphabets.                                   | dynamsoft-label-recognizer     |
| **RecognizeUppercaseLetters**           | Focuses on recognizing uppercase English alphabets.                              | dynamsoft-label-recognizer     |
| **Default**                             | Versatile function for barcode reading, document detection, or text recognition. | Any of the above three modules |