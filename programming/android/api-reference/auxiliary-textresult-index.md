---
layout: default-layout
title: Dynamsoft Barcode Reader Android API Reference - TextResult index
description: This page shows the TextResult index of Dynamsoft Barcode Reader for Android SDK.
keywords: TextResult index, api reference, android
needAutoGenerateSidebar: true
needGenerateH3Content: false
---

# Barcode Result Classes

## [TextResult](auxiliary-TextResult.md)

```java
import com.dynamsoft.dbr.TextResult;
```

| Attribute | Type | Descriptions |
| --------- | ---- | ------------ |
| [`barcodeFormat`](auxiliary-TextResult.md#barcodeformat) | *int* | Barcode type in BarcodeFormat group 1. |
| [`barcodeFormatString`](auxiliary-TextResult.md#barcodeformatstring) | *String* | Barcode type in BarcodeFormat group 1 as string. |
| [`barcodeFormat_2`](auxiliary-TextResult.md#barcodeformat_2) | *int* | Barcode type in BarcodeFormat group 2. |
| [`barcodeFormatString_2`](auxiliary-TextResult.md#barcodeformatstring_2) | *String* | Barcode type in BarcodeFormat group 2 as string. |
| [`barcodeText`](auxiliary-TextResult.md#barcodetext) | *String* | The barcode text, ends by '\0'. |
| [`barcodeBytes`](auxiliary-TextResult.md#barcodebytes) | *byte\[\]* | The barcode content in a byte array. |
| [`localizationResult`](auxiliary-TextResult.md#localizationresult) | [`LocalizationResult`](auxiliary-LocalizationResult.md)\* | The corresponding localization result. |
| [`detailedResult`](auxiliary-TextResult.md#detailedresult) | *Object* | One of the following: [`QRCodeDetails`](auxiliary-qrcodedetails.md), [`PDF417Details`](auxiliary-pdf417details.md), [`DataMatrixDetails`](auxiliary-datamatrixdetails.md), [`AztecDetails`](auxiliary-aztecdetails.md), [`OneDCodeDetails`](auxiliary-onedcodedetails.md). |
| [`results`](auxiliary-TextResult.md#results) | [`ExtendedResult`](auxiliary-ExtendedResult.md)\[\] | The extended result array. |
| [`exception`](auxiliary-TextResult.md#exception) | *String* | The exception message. |
| [`isDPM`](auxiliary-TextResult.md#isdpm) | *int* | This attribute stands for whether the result is a DPM result. |
| [`isMirrored`](auxiliary-TextResult.md#ismirrored) | *int* | This attribute stands for whether the barcode is mirrored. |

```java
// Get the text result by decode methodes
TextResult[] textresult = barcodeReader.decodeBuffer(frame.getData(),frame.getWidth(),frame.getHeight(),frame.getStrides()[0],frame.getFormat(),"");
```

## [LocalizationResult](auxiliary-LocalizationResult.md)

```java
import com.dynamsoft.dbr.LocalizationResult;
```

`LocalizationResult` is the extension of the class [`TextResult`](auxiliary-TextResult.md). It stores the localization result information.

| Attribute | Type | Description |
|---------- | ---- | ----------- |
| [`terminatePhase`](auxiliary-LocalizationResult.md#terminatephase) | *int* | The terminate phase of localization result. |
| [`barcodeFormat`](auxiliary-LocalizationResult.md#barcodeformat) | *int* | Barcode type in BarcodeFormat group 1. |
| [`barcodeFormatString`](auxiliary-LocalizationResult.md#barcodeformatstring) | *String* | Barcode type in BarcodeFormat group 1 as string. |
| [`barcodeFormat_2`](auxiliary-LocalizationResult.md#barcodeformat_2) | *int* | Barcode type in BarcodeFormat group 2. |
| [`barcodeFormatString_2`](auxiliary-LocalizationResult.md#barcodeformatstring_2) | *String* | Barcode type in BarcodeFormat group 2 as string. |
| [`resultPoints`](auxiliary-LocalizationResult.md#resultpoints) | [`Point`](auxiliary-Point.md)\[\] | The vertices coordinates information of the barcode region. |
| [`angle`](auxiliary-LocalizationResult.md#angle) | *int* | The angle of a barcode. Values range is from 0 to 360. |
| [`moduleSize`](auxiliary-LocalizationResult.md#modulesize) | *int* | The barcode module size (the minimum bar width in pixel). |
| [`pageNumber`](auxiliary-LocalizationResult.md#oagenumber) | *int* | The page number the barcode located in. The index is 0-based. |
| [`regionName`](auxiliary-LocalizationResult.md#regionname) | *String* | The region name the barcode located in. |
| [`documentName`](auxiliary-LocalizationResult.md#documentname) | *String* | The document name. |
| [`resultCoordinateType`](auxiliary-LocalizationResult.md#resultcoordinatetype) | *int* | The coordinate type. |
| [`accompanyingTextBytes`](auxiliary-LocalizationResult.md#accompanyingtextbytes) | *byte\[\]* | The accompanying text content in a byte array. |
| [`confidence`](auxiliary-LocalizationResult.md#confidence) | *int* | The confidence of the localization result. |

```java
if ( textresult != null && textresult.length != 0){
    for ( int i = 0; i< textresult.length; i++ ) {
        LocalizationResult localizationResult = textresult[i].localizationResult;
        // DO something on localization results.
    }
}
```

## [ExtendedResult](auxiliary-ExtendedResult.md)

```java
import com.dynamsoft.dbr.ExtendedResult;
```

`ExtendedResult` is the extension of the class [`TextResult`](auxiliary-TextResult.md). It stores the extended result information.
  
| Attribute | Type | Description |
|---------- |------|-------------|
| [`resultType`](auxiliary-ExtendedResult.md#resulttype) | *int* | The extended result type. |
| [`barcodeFormat`](auxiliary-ExtendedResult.md#barcodeformat) | *int* | Barcode type in BarcodeFormat group 1. |
| [`barcodeFormatString`](auxiliary-ExtendedResult.md#barcodeformatstring) | *String* | Barcode type in BarcodeFormat group 1 as string. |
| [`barcodeFormat_2`](auxiliary-ExtendedResult.md#barcodeformat_2) | *int* | Barcode type in BarcodeFormat group 2. |
| [`barcodeFormatString_2`](auxiliary-ExtendedResult.md#barcodeformatstring_2) | *String* | Barcode type in BarcodeFormat group 2 as string. |
| [`confidence`](auxiliary-ExtendedResult.md#confidence) | *int* | The confidence of the result. The higher confidence means the higher accuracy. |
| [`bytes`](auxiliary-ExtendedResult.md#bytes) | *byte\[\]* | The content in a byte array. |
| [`accompanyingTextBytes`](auxiliary-ExtendedResult.md#accompanyingtextbytes) | *byte\[\]* | The accompanying text content in a byte array. |
| [`deformation`](auxiliary-ExtendedResult.md#deformation) | *int* | The deformation value. |
| [`detailedResult`](auxiliary-ExtendedResult.md#detailedresult) | *Object* | One of the following: [`QRCodeDetails`](auxiliary-qrcodedetails.md), [`PDF417Details`](auxiliary-pdf417details.md), [`DataMatrixDetails`](auxiliary-datamatrixdetails.md), [`AztecDetails`](auxiliary-aztecdetails.md), [`OneDCodeDetails`](auxiliary-onedcodedetails.md). |
| [`samplingImage`](auxiliary-ExtendedResult.md#samplingimage) | [`SamplingImageData`](auxiliary-samplingimagedata.md) | The sampling image info. |
| [`clarity`](auxiliary-ExtendedResult.md#clarity) | *int* | The clarity of the barcode zone in percentage. |

```java
if ( textresult != null && textresult.length != 0){
    for ( int i = 0; i < textresult.length; i++ ) {
        ExtendedResult[] extendedResult = textresult[i].results;
        // Do something on extended results.
    }
}
```

## [AztecDetails](auxiliary-AztecDetails.md)

```java
import com.dynamsoft.dbr.AztecDetails;
```

`AztecDetails` is one of the [`detailedResult`](auxiliary-TextResult.md#detailedresult) in class `TextResult`. It stores the Aztec code details.
  
| Attribute | Type | Description |
|---------- | -----|------ |
| [`moduleSize`](auxiliary-AztecDetails.md#modulesize) | *int* | The barcode module size (the minimum bar width in pixel). |
| [`rows`](auxiliary-AztecDetails.md#rows) | *int* | The row count of the barcode. |
| [`columns`](auxiliary-AztecDetails.md#columns) | *int* | The column count of the barcode. |
| [`layerNumber`](auxiliary-AztecDetails.md#layernumber) | *int* | A negative number (-1, -2, -3, -4) specifies a compact Aztec code. A positive number (1, 2, .. 32) specifies a normal (full-rang) Aztec code. |

```java
//The textresult[i] is one of the text result you got  
AztecDetails aztecDetails = (AztecDetails) textresult[i].detailedResult;
```

## [DataMatrixDetails](auxiliary-DataMatrixDetails.md)

```java
import com.dynamsoft.dbr.DataMatrixDetails;
```

`DataMatrixDetails` is one of the [`detailedResult`](auxiliary-TextResult.md#detailedresult) in class `TextResult`. It stores the DataMatrix code details.
  
| Attribute | Type | Description |
|---------- |-----|------|
| [`moduleSize`](auxiliary-DataMatrixDetails.md#modulesize) | *int* | The barcode module size (the minimum bar width in pixel). |
| [`rows`](auxiliary-DataMatrixDetails.md#rows) | *int* | The row count of the barcode. |
| [`columns`](auxiliary-DataMatrixDetails.md#columns) | *int* | The column count of the barcode. |
| [`dataRegionRows`](auxiliary-DataMatrixDetails.md#dataregionrows) | *int* | The data region row count of the barcode. |
| [`dataRegionColumns`](auxiliary-DataMatrixDetails.md#dataregioncolumns) | *int* | The data region column count of the barcode. |
| [`dataRegionNumber`](auxiliary-DataMatrixDetails.md#dataregionnumber) | *int* | The data region count. |

```java
//The textresult[i] is one of the text result you got  
DataMatrixDetails dataMatrixDetails = (DataMatrixDetails) textresult[i].detailedResult;
```

## [OneDCodeDetails](auxiliary-OneDCodeDetails.md)

```java
import com.dynamsoft.dbr.OneDCodeDetails;
```

`OneDCodeDetails` is one of the [`detailedResult`](auxiliary-TextResult.md#detailedresult) in class `TextResult`. It stores the OneD code details.

| Attribute | Type | Description |
|---------- |-----| ---- |
| [`moduleSize`](auxiliary-OneDCodeDetails.md#modulesize) | *int* | The barcode module size (the minimum bar width in pixel). |
| [`startCharsBytes`](auxiliary-OneDCodeDetails.md#startcharsbytes) | *int* | The start chars in a byte array. |
| [`stopCharsBytes`](auxiliary-OneDCodeDetails.md#stopcharsbytes) | *int* | The stop chars in a byte array. |
| [`checkDigitBytes`](auxiliary-OneDCodeDetails.md#checkdigitbytes) | *int* | The check digit chars in a byte array. |
| [`startPatternRange`](auxiliary-OneDCodeDetails.md#startpatternrange) | *int* | The start pattern range of the OneDcode. |
| [`middlePatternRange`](auxiliary-OneDCodeDetails.md#middlepatternrange) | *int* | The middle pattern range of the OneDcode. |
| [`endPatternRange`](auxiliary-OneDCodeDetails.md#endpatternrange) | *int* | The end pattern range of the OneDcode. |

```java
//The textresult[i] is one of the text result you got  
OneDCodeDetails oneDDetails = (OneDCodeDetails) textresult[i].detailedResult;
```

## [PDF417Details](auxiliary-PDF417Details.md)

```java
import com.dynamsoft.dbr.PDF417Details;
```

`PDF417Details` is one of the [`detailedResult`](auxiliary-TextResult.md#detailedresult) in class `TextResult`. It stores the PDF417 code details.
  
| Attribute | Type | Description |
|---------- |------|------------ |
| [`moduleSize`](auxiliary-PDF417Details.md#modulesize) | *int* | The barcode module size (the minimum bar width in pixel). |
| [`rows`](auxiliary-PDF417Details.md#rows) | *int* | The row count of the barcode. |
| [`columns`](auxiliary-PDF417Details.md#columns) | *int* | The column count of the barcode. |
| [`errorCorrectionLevel`](auxiliary-PDF417Details.md#errorcorrectionlevel) | *int* | The error correction level of the barcode. |

```java
//The textresult[i] is one of the text results you got  
PDF417Details pdf417Details = (PDF417Details) textresult[i].detailedResult;
```

## [QRCodeDetails](auxiliary-QRCodeDetails.md)

```java
import com.dynamsoft.dbr.QRCodeDetails;
```

`QRCodeDetails` is one of the [`detailedResult`](auxiliary-TextResult.md#detailedresult) in class `TextResult`. It stores the QRCode details.
  
| Attribute | Type | Description |
|---------- | ---- |-----|
| [`moduleSize`](auxiliary-QRCodeDetails.md#modulesize) | *int* | The barcode module size (the minimum bar width in pixels). |
| [`rows`](auxiliary-QRCodeDetails.md#rows) | *int* | The row count of the barcode.   |
| [`columns`](auxiliary-QRCodeDetails.md#columns) | *int* | The column count of the barcode. |
| [`errorCorrectionLevel`](auxiliary-QRCodeDetails.md#errorcorrectionlevel) | *int* | The error correction level of the barcode.   |
| [`version`](auxiliary-QRCodeDetails.md#version) | *int* | The version of the QR Code. |
| [`model`](auxiliary-QRCodeDetails.md#model) | *int* | Number of the models. |
| [`mode`](auxiliary-QRCodeDetails.md#mode) | *int* | Identify the first data encoding mode. |
| [`page`](auxiliary-QRCodeDetails.md#page) | *int* | Identify the position of the particular symbol. |
| [`totalPage`](auxiliary-QRCodeDetails.md#totalpage) | *int* | Identify the total number of symbols to be concatenated in the Structured Append format. |
| [`parityData`](auxiliary-QRCodeDetails.md#paritydata) | *int* | The Parity Data shall be an 8 bit byte following the Symbol Sequence Indicator. The parity data is a value obtained by XORing byte by byte the ASCII/JIS values of all the original input data before division into symbol blocks. |

```java
//The textresult[i] is one of the text results you got  
QRCodeDetails qrDetails = (QRCodeDetails) textresult[i].detailedResult;
```

## [SamplingImageData](auxiliary-SamplingImageData.md)

```java
import com.dynamsoft.dbr.SamplingImageData;
```

`SamplingImageData` stores the detailed image data in `ExtendedResult`.

| Attribute | Type | Description |
|---------- | ---- | ----------- |
| [`bytes`](#bytes) | *byte\[\]* | The sampling image data in a byte array. |
| [`width`](#width) | *int* | The width of the sampling image. |
| [`height`](#height) | *int* | The height of the sampling image. |

```java
SamplingImageData samplingImageData = extendedResult[j].samplingImage;
```
