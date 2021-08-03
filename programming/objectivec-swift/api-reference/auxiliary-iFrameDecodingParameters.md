---
layout: default-layout
title: Dynamsoft Barcode Reader Objective-C & Swift API Reference - iFrameDecodingParameters Class
description: This page shows the iFrameDecodingParameters Class of Dynamsoft Barcode Reader for iOS SDK.
keywords: iExtendedResult, class, api reference, objective-c, oc, swift
needAutoGenerateSidebar: true
noTitleIndex: true
---


# Class iFrameDecodingParameters

Defines a struct to configure the frame decoding Parameters.  

## Typedefs

```objc
@interface iFrameDecodingParameters
```

| Attribute | Type | Descriptions |
|---------- | ---- | ------------ |
| [`maxQueueLength`](#maxqueuelength) | *NSInteger* | The maximum number of frames waiting for decoding. |
| [`maxResultQueueLength`](#maxresultqueuelength) | *NSInteger* | The maximum number of frames waiting results (text result/localization result) will be kept for further reference. |
| [`width`](#width) | *NSInteger* | The width of the frame image in pixels.  |
| [`height`](#height) | *NSInteger* | The height of the frame image in pixels. |
| [`stride`](#stride) | *NSInteger* | The stride (or scan width) of the frame image. |
| [`imagePixelFormat`](#imagepixelformat) | [`EnumImagePixelFormat`]({{ site.enumerations }}other-enums.html#imagepixelformat) | The image pixel format used in the image byte array. |
| [`region`](#region) | [`iRegionDefinition`](auxiliary-iRegionDefinition.md) | The region definition of the frame to calculate the internal indicator. |
| [`threshold`](#threshold) | *float* | The threshold used for filtering frames. |
| [`fps`](#fps) | *NSInteger* | The frequency of calling [`appendFrame`]({{site.android_methods}}primary-video.html#appendframe) per second. |
| [`autoFilter`](#autofilter) | *NSInteger* | Sets whether to filter frames automatically. |
| [`clarityCalculationMethod`](#claritycalculationmethod) | [`EnumClarityCalculationMethod`]({{ site.enumerations }}frame-decoding-enums.html#claritycalculationmethod) | Sets the method used for calculating the clarity of the frames. |
| [`clarityFilterMode`](#clarityfiltermode) | [`EnumClarityFilterMode`]({{ site.enumerations }}frame-decoding-enums.html#clarityfiltermode) | Sets the mode used for filtering frames by calculated clarity. |

## maxQueueLength

The maximum number of frames waiting for decoding.

```objc
NSInteger maxQueueLength
```

**Value range**
[0,0x7fffffff]

**Default value**
3

## maxResultQueueLength

The maximum number of frames waiting results (text result/localization result) will be kept for further reference.  

```objc
NSInteger maxResultQueueLength
```

**Value range**
[0,0x7fffffff]

**Default value**
10  

## width

The width of the frame image in pixels.

```objc
NSInteger width
```

**Value range**
[0,0x7fffffff]

**Default value**
0  

## height

The height of the frame image in pixels.

```objc
NSInteger height
```

**Value range**
[0,0x7fffffff]

**Default value**
0  

## stride

The stride (or scan width) of the frame image.

```objc
NSInteger stride
```

**Value range**
[0,0x7fffffff]

**Default value**
0

## imagePixelFormat

The image pixel format used in the image byte array.

```objc
EnumImagePixelFormat imagePixelFormat
```

**Value range**
A value of [`EnumImagePixelFormat`]({{ site.enumerations }}other-enums.html#imagepixelformat) Enumeration items.

**Default value**
`EnumImagePixelFormatGrayScaled`

**See also**  
[`EnumImagePixelFormat`]({{ site.enumerations }}other-enums.html#imagepixelformat)

## region

The region definition of the frame to calculate the internal indicator. 

```objc
iRegionDefinition region
```

**Default value**  
`{ regionLeft = 0, regionRight = 100, regionTop = 0, regionBottom = 100, regionMeasuredByPercentage = 1 }`

**See also**
[`iRegionDefinition`](iRegionDefinition.md)

## threshold

The threshold used for filtering frames.

```objc
float threshold
```

**Value range**
[0, 1]

**Default value**
0.1

**Remarks**  
The SDK will calculate an inner indicator for each frame from [`AppendFrame`](../methods/video.md#appendframe), if the change rate of the indicators between the current frame and the history frames is larger than the given threshold, the current frame will not be added to the inner frame queue waiting for decoding.

## fps

The frequency of calling [`AppendFrame`](../methods/video.md#appendframe) per second.

```objc
NSInteger fps
```

**Value range**
[0,0x7fffffff]

**Default value**
0  

**Remarks**  
0 means the frequency will be calculated automatically by the SDK.

## autoFilter

Sets whether to filter frames automatically.

```objc
NSInteger autoFilter
```

**Value range**
[0,1]

**Default value**
1  

**Remarks**
0: Diable filtering frames automatically. 1: Enable filtering frames automatically. 

## clarityCalculationMethod

Sets the method used for calculating the clarity of the frames.

```objc
EnumClarityCalculationMethod clarityCalculationMethod
```

**Value range**
Any one of the [`EnumClarityCalculationMethod`]({{ site.enumerations }}frame-decoding-enums.html#claritycalculationmethod) Enumeration items.

**Default value**
EnumClarityCalculationMethodContrast

**See also**  
[`EnumClarityCalculationMethod`]({{ site.enumerations }}frame-decoding-enums.html#claritycalculationmethod)

## clarityFilterMode

Sets the mode used for filtering frames by calculated clarity.

```objc
EnumClarityFilterMode clarityFilterMode
```

**Value range**
Any one of the [`EnumClarityFilterMode`]({{ site.enumerations }}frame-decoding-enums.html#clarityfiltermode) Enumeration items.

**Default value**
EnumClarityFilterModeGeneral

**See also**  
[`EnumClarityFilterMode`]({{ site.enumerations }}frame-decoding-enums.html#clarityfiltermode)
