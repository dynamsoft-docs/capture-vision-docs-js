---
layout: default-layout
title: PresetTemplate - Dynamsoft Vision Router Enumerations
description: The enumeration PresetTemplate of Dynamsoft Vision Router describes the preset template.
keywords: Capture state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Enumeration PresetTemplate

`PresetTemplate` describes the preset template names.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumPresetTemplate {
  /**
   * @brief Versatile function for barcode reading, document detection, or text recognition.
   */
  PT_DEFAULT = "Default",
  /**
   * @brief Scans a single barcode.
   */
  PT_READ_BARCODES = "ReadBarcodes_Default",
  /**
   * @brief Identifies and reads any text present.
   */
  PT_RECOGNIZE_TEXT_LINES = "RecognizeTextLines_Default",
  /**
   * @brief RIdentifies the edges of a document.
   */
  PT_DETECT_DOCUMENT_BOUNDARIES = "DetectDocumentBoundaries_Default",
  /**
   * @brief Detects document edges and standardizes its format.
   */
  PT_DETECT_AND_NORMALIZE_DOCUMENT = "DetectAndNormalizeDocument_Default",
  /**
   * @brief Adjusts a document to a standard format using detected borders.
   */
  PT_NORMALIZE_DOCUMENT = "NormalizeDocument_Default",
  /**
   * @brief Represents a barcode reading mode where speed is prioritized.
   *
   * In this mode, the barcode reader will optimize for faster barcode detection
   * and decoding, sacrificing some level of accuracy and read rate. It is suitable
   * for situations where a quick response time is more important than perfect
   * barcode recognition.
   */
  PT_READ_BARCODES_SPEED_FIRST = "ReadBarcodes_SpeedFirst",
  /**
   * @brief Represents a barcode reading mode where barcode read rate is prioritized.
   *
   * In this mode, the barcode reader will optimize for higher barcode read rates,
   * even if it may sometimes result in reduced accuracy and speed. It is suitable for
   * scenarios where maximizing the number of successfully read barcodes is critical.
   */
  PT_READ_BARCODES_READ_RATE_FIRST = "ReadBarcodes_ReadRateFirst",
  /**
   * @brief Represents a balanced barcode reading mode.
   *
   * This mode aims for a reasonable balance between speed and read rate in barcode
   * recognition. It is suitable for most common use cases where a compromise between
   * speed and read rate is acceptable.
   */
  PT_READ_BARCODES_BALANCE = "ReadBarcodes_Balance",
  /**
  * @brief Represents a barcode reading mode for single barcode code detection.
  *
  * In this mode, the barcode reader will focus on detecting and decoding a single
  * barcode code, ignoring any additional codes in the same image. It is efficient
  * when the target image has only one barcode.
  */
  PT_READ_SINGLE_BARCODE = "ReadSingleBarcode",
  /**
   * @brief Represents a barcode reading mode optimized for dense barcode codes.
   *
   * This mode is designed to handle dense or closely packed barcode codes where
   * accuracy is paramount. It may operate slower than other modes but is suitable
   * for challenging scenarios where code density is high.
   */
  PT_READ_DENSE_BARCODES = "ReadDenseBarcodes",
  /**
   * @brief Represents a barcode reading mode optimized for distant barcode codes.
   *
   * This mode is designed to scanning a barcode that is placed far from the device.
   */
  PT_READ_DISTANT_BARCODES = "ReadDistantBarcodes",
  /**
  * @brief Represents a text recognition mode focused on recognizing numbers.
  */
  PT_RECOGNIZE_NUMBERS = "RecognizeNumbers",
  /**
   * @brief Represents a text recognition mode focused on recognizing alphabetic characters (letters).
   *
   */
  PT_RECOGNIZE_LETTERS = "RecognizeLetters",
  /**
   * @brief Represents a text recognition mode that combines numbers and alphabetic characters (letters) recognition.
   */
  PT_RECOGNIZE_NUMBERS_AND_LETTERS = "RecognizeNumbersAndLetters",
  /**
   * @brief Represents a text recognition mode that combines numbers and uppercase letters recognition.
   */
  PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS = "RecognizeNumbersAndUppercaseLetters",
  /**
   * @brief Represents a text recognition mode focused on recognizing uppercase letters.
   */
  PT_RECOGNIZE_UPPERCASE_LETTERS = "RecognizeUppercaseLetters"
}
```