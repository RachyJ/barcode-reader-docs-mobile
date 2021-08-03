---
layout: default-layout
title: Dynamsoft Barcode Reader Objective-C & Swift API Reference - iFurtherModes Class
description: This page shows the iFurtherModes Class of Dynamsoft Barcode Reader for iOS SDK.
keywords: iFurtherModes, class, api reference, objective-c, oc, swift
needAutoGenerateSidebar: true
noTitleIndex: true
---


# Class iFurtherModes

Stores the FurtherModes.

## Typedefs

```objc
@interface iFurtherModes
```  

| Attribute | Type | Descriptions |
|---------- | ---- | ----- |
| [`colourClusteringModes`](auxiliary-iFurtherModes.md#colourclusteringmodes) | *NSArray*\* | Sets the mode and priority for colour categorization. |
| [`colourConversionModes`](auxiliary-iFurtherModes.md#colourconversionmodes) | *NSArray*\* | Sets the mode and priority for converting a colour image to a grayscale image. |
| [`grayscaleTransformationModes`](auxiliary-iFurtherModes.md#grayscaletransformationmodes) | *NSArray*\* | Sets the mode and priority for the grayscale image conversion. |
| [`regionPredetectionModes`](auxiliary-iFurtherModes.md#regionpredetectionmodes) | *NSArray*\* | Sets the region pre-detection mode for barcodes search. |
| [`imagePreprocessingModes`](auxiliary-iFurtherModes.md#imagepreprocessingmodes) | *NSArray*\* | Sets the mode and priority for image preprocessing algorithms. |
| [`textureDetectionModes`](auxiliary-iFurtherModes.md#texturedetectionmodes) | *NSArray*\* | Sets the mode and priority for texture detection. |
| [`textFilterModes`](auxiliary-iFurtherModes.md#textfiltermodes) | *NSArray*\* | Sets the mode and priority for text filter. |
| [`dpmCodeReadingModes`](auxiliary-iFurtherModes.md#dpmcodereadingmodes) | *NSArray*\* | Sets the mode and priority for DPM code reading. |
| [`deformationResistingModes`](auxiliary-iFurtherModes.md#deformationresistingmodes) | *NSArray*\* | Sets the mode and priority for deformation resisting. |
| [`barcodeComplementModes`](auxiliary-iFurtherModes.md#barcodecomplementmodes) | *NSArray*\* | Sets the mode and priority to complement the missing parts in the barcode. |
| [`barcodeColourModes`](auxiliary-iFurtherModes.md#barcodecolourmodes) | *NSArray*\* | Sets the mode and priority for the barcode colour mode used to process the barcode zone. |
| [`accompanyingTextRecognitionModes`](auxiliary-iFurtherModes.md#accompanyingtextrecognitionmodes) | *NSArray*\* | Sets the mode and priority to recognize accompanying text. |

## colourClusteringModes

Sets the mode and priority for colour categorization. Not supported yet.  

```objc
NSArray* colourClusteringModes[8]
```

**Value range**  
Each array item can be any one of the [`EnumColourClusteringMode`]({{ site.enumerations }}parameter-mode-enums.html#colourclusteringmode) Enumeration items.  

**Default value**  
`[EnumColourClusteringModeSkip, EnumColourClusteringModeSkip, EnumColourClusteringModeSkip, EnumColourClusteringModeSkip, EnumColourClusteringModeSkip, EnumColourClusteringModeSkip, EnumColourClusteringModeSkip, EnumColourClusteringModeSkip]`  

**Remarks**  
The array index represents the priority of the item. The smaller index is, the higher priority is.

**See also**  
[`EnumColourClusteringMode`]({{ site.enumerations }}parameter-mode-enums.html#colourclusteringmode)

## colourConversionModes

Sets the mode and priority for converting a colour image to a grayscale image.

```objc
NSArray* colourConversionModes[8]
```

**Value range**  
Each array item can be any one of the [`EnumColourConversionMode`]({{ site.enumerations }}parameter-mode-enums.html#colourconversionmode) Enumeration items.

**Default value**  
`[EnumColourConversionModeGeneral, EnumColourConversionModeSkip, EnumColourConversionModeSkip, EnumColourConversionModeSkip, EnumColourConversionModeSkip, EnumColourConversionModeSkip, EnumColourConversionModeSkip, EnumColourConversionModeSkip]`

**Remarks**  
The array index represents the priority of the item. The smaller index is, the higher priority is.  

**See also**  
[`EnumColourConversionMode`]({{ site.enumerations }}parameter-mode-enums.html#colourconversionmode)

## grayscaleTransformationModes

Sets the mode and priority for the grayscale image conversion.

```objc
NSArray* grayscaleTransformationModes[8]
```

**Value range**  
Each array item can be any one of the [`EnumGrayscaleTransformationMode`]({{ site.enumerations }}parameter-mode-enums.html#grayscaletransformationmode) Enumeration items.

**Default value**  
`[EnumGrayscaleTransformationModeOriginal, EnumGrayscaleTransformationModeSkip, EnumGrayscaleTransformationModeSkip, EnumGrayscaleTransformationModeSkip, EnumGrayscaleTransformationModeSkip, EnumGrayscaleTransformationModeSkip, EnumGrayscaleTransformationModeSkip, EnumGrayscaleTransformationModeSkip]`  

**Remarks**  
The array index represents the priority of the item. The smaller index is, the higher priority is.  

**See also**  
[`EnumGrayscaleTransformationMode`]({{ site.enumerations }}parameter-mode-enums.html#grayscaletransformationmode)

## regionPredetectionModes

Sets the region pre-detection mode for barcodes search.

```objc
NSArray* regionPredetectionModes[8]
```

**Value range**  
Each array item can be any one of the [`EnumRegionPredetectionMode`]({{ site.enumerations }}parameter-mode-enums.html#regionpredetectionmode) Enumeration items.  

**Default value**  
`[EnumRegionPredetectionModeGeneral, EnumRegionPredetectionModeSkip, EnumRegionPredetectionModeSkip, EnumRegionPredetectionModeSkip, EnumRegionPredetectionModeSkip, EnumRegionPredetectionModeSkip, EnumRegionPredetectionModeSkip, EnumRegionPredetectionModeSkip]`

**Remarks**  
The array index represents the priority of the item. The smaller index is, the higher priority is. If the image is large and the barcode on the image is very small, it is recommended to enable region predetection to speed up the localization process and recognition accuracy.

**See also**  
[`EnumRegionPredetectionMode`]({{ site.enumerations }}parameter-mode-enums.html#regionpredetectionmode)

## imagePreprocessingModes

Sets the mode and priority for image preprocessing algorithms.

```objc
NSArray* imagePreprocessingModes[8]
```

**Value range**  
Each array item can be any one of the [`EnumImagePreprocessingMode`]({{ site.enumerations }}parameter-mode-enums.html#imagepreprocessingmode) Enumeration items.  

**Default value**  
`[EnumImagePreprocessingModeGeneral, EnumImagePreprocessingModeSkip, EnumImagePreprocessingModeSkip, EnumImagePreprocessingModeSkip, EnumImagePreprocessingModeSkip, EnumImagePreprocessingModeSkip, EnumImagePreprocessingModeSkip, EnumImagePreprocessingModeSkip]`

**Remarks**  
The array index represents the priority of the item. The smaller index is, the higher priority is.

**See also**  
[`EnumImagePreprocessingMode`]({{ site.enumerations }}parameter-mode-enums.html#imagepreprocessingmode)

## textureDetectionModes

Sets the mode and priority for texture detection.

```objc
NSArray* textureDetectionModes[8]
```

**Value range**  
Each array item can be any one of the [`EnumTextureDetectionMode`]({{ site.enumerations }}parameter-mode-enums.html#texturedetectionmode) Enumeration items.  

**Default value**  
`[EnumTextureDetectionModeGeneralWidthConcentration, EnumTextureDetectionModeSkip, EnumTextureDetectionModeSkip, EnumTextureDetectionModeSkip, EnumTextureDetectionModeSkip, EnumTextureDetectionModeSkip, EnumTextureDetectionModeSkip, EnumTextureDetectionModeSkip]`  

**Remarks**  
The array index represents the priority of the item. The smaller index is, the higher priority is.

**See also**  
[`EnumTextureDetectionMode`]({{ site.enumerations }}parameter-mode-enums.html#texturedetectionmode)

## textFilterModes

Sets the mode and priority for text filter.

```objc
NSArray* textFilterModes[8]
```

**Value range**  
Each array item can be any one of the [`EnumTextFilterMode`]({{ site.enumerations }}parameter-mode-enums.html#textfiltermode) Enumeration items.  

**Default value**  
`[EnumTextFilterModeGeneralContour, EnumTextFilterModeSkip, EnumTextFilterModeSkip, EnumTextFilterModeSkip, EnumTextFilterModeSkip, EnumTextFilterModeSkip, EnumTextFilterModeSkip, EnumTextFilterModeSkip]`

**Remarks**  
The array index represents the priority of the item. The smaller index is, the higher priority is. If the image contains a lot of text, you can enable text filter to speed up the localization process.

**See also**  
[`EnumTextFilterMode`]({{ site.enumerations }}parameter-mode-enums.html#textfiltermode)

## dpmCodeReadingModes

Sets the mode and priority for DPM code reading.

```objc
NSArray* dpmCodeReadingModes[8]
```

**Value range**  
Each array item can be any one of the [`EnumDPMCodeReadingMode`]({{ site.enumerations }}parameter-mode-enums.html#dpmcodereadingmode) Enumeration items.  

**Default value**  
`[EnumDPMCodeReadingModeSkip, EnumDPMCodeReadingModeSkip, EnumDPMCodeReadingModeSkip, EnumDPMCodeReadingModeSkip, EnumDPMCodeReadingModeSkip, EnumDPMCodeReadingModeSkip, EnumDPMCodeReadingModeSkip, EnumDPMCodeReadingModeSkip]`  

**Remarks**  
The array index represents the priority of the item. The smaller index is, the higher priority is.  

**See also**  
[`EnumDPMCodeReadingMode`]({{ site.enumerations }}parameter-mode-enums.html#dpmcodereadingmode)

## deformationResistingModes

Sets the mode and priority for deformation resisting.

```objc
NSArray* deformationResistingModes[8]
```

**Value range**  
Each array item can be any one of the [`EnumDeformationResistingMode`]({{ site.enumerations }}parameter-mode-enums.html#deformationresistingmode) Enumeration items.  

**Default value**  
`[EnumDeformationResistingModeSkip, EnumDeformationResistingModeSkip, EnumDeformationResistingModeSkip, EnumDeformationResistingModeSkip, EnumDeformationResistingModeSkip, EnumDeformationResistingModeSkip, EnumDeformationResistingModeSkip, EnumDeformationResistingModeSkip]`  

**Remarks**  
The array index represents the priority of the item. The smaller index is, the higher priority is.  

**See also**  
[`EnumDeformationResistingMode`]({{ site.enumerations }}parameter-mode-enums.html#deformationresistingmode)

## barcodeComplementModes

Sets the mode and priority to complement the missing parts in the barcode.

```objc
NSArray* barcodeComplementModes[8]
```

**Value range**  
Each array item can be any one of the [`EnumBarcodeComplementMode`]({{ site.enumerations }}parameter-mode-enums.html#barcodecomplementmode) Enumeration items.  

**Default value**  
`[EnumBarcodeComplementModeSkip, EnumBarcodeComplementModeSkip, EnumBarcodeComplementModeSkip, EnumBarcodeComplementModeSkip, EnumBarcodeComplementModeSkip, EnumBarcodeComplementModeSkip, EnumBarcodeComplementModeSkip, EnumBarcodeComplementModeSkip]`  

**Remarks**  
The array index represents the priority of the item. The smaller index is, the higher priority is.  

**See also**  
[`EnumBarcodeComplementMode`]({{ site.enumerations }}parameter-mode-enums.html#barcodecomplementmode)

## barcodeColourModes

Sets the mode and priority for the barcode colour mode used to process the barcode zone.

```objc
NSArray* barcodeColourModes[8]
```

**Value range**  
Each array item can be any one of the [`EnumBarcodeColourMode`]({{ site.enumerations }}parameter-mode-enums.html#barcodecolourmode) Enumeration items.  

**Default value**  
`[EnumBarcodeColourModeDarkOnLight, EnumBarcodeColourModeSkip, EnumBarcodeColourModeSkip, EnumBarcodeColourModeSkip, EnumBarcodeColourModeSkip, EnumBarcodeColourModeSkip, EnumBarcodeColourModeSkip, EnumBarcodeColourModeSkip]`

**Remarks**  
The array index represents the priority of the item. The smaller index is, the higher priority is.  

**See also**  
[`EnumBarcodeColourMode`]({{ site.enumerations }}parameter-mode-enums.html#barcodecolourmode)

## accompanyingTextRecognitionModes

Sets the mode and priority to recognize accompanying text.

```objc
NSArray* accompanyingTextRecognitionModes[8]
```

**Value range**  
Each array item can be any one of the [`EnumAccompanyingTextRecognitionMode`]({{ site.enumerations }}parameter-mode-enums.html#accompanyingtextrecognitionmode) Enumeration items.  

**Default value**  
`[EnumAccompanyingTextRecognitionModeSkip, EnumAccompanyingTextRecognitionModeSkip, EnumAccompanyingTextRecognitionModeSkip, EnumAccompanyingTextRecognitionModeSkip, EnumAccompanyingTextRecognitionModeSkip,  EnumAccompanyingTextRecognitionModeSkip, EnumAccompanyingTextRecognitionModeSkip, EnumAccompanyingTextRecognitionModeSkip]`  

**Remarks**  
The array index represents the priority of the item. The smaller index is, the higher priority is.  

**See also**  
[`EnumAccompanyingTextRecognitionMode`]({{ site.enumerations }}parameter-mode-enums.html#accompanyingtextrecognitionmode)
