---
layout: default-layout
title: Dynamsoft Barcode Reader Objective-C & Swift API Reference - iRegionDefinition Class
description: This page shows the iRegionDefinition Class of Dynamsoft Barcode Reader for iOS SDK.
keywords: iRegionDefinition, class, api reference, objective-c, oc, swift
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Class iRegionDefinition

Stores the region information.  

## Typedefs

```objc
@interface iRegionDefinition
```  

| Attribute | Type | Descriptions |
|---------- | ---- | ------------ |
| [`regionTop`](auxiliary-RegionDefinition.md#regiontop) | *NSInteger* | The top-most coordinate or percentage of the region. |
| [`regionLeft`](auxiliary-RegionDefinition.md#regionleft) | *NSInteger* | The Left-most coordinate or percentage of the region. |
| [`regionRight`](auxiliary-RegionDefinition.md#regionright) | *NSInteger* | The Right-most coordinate or percentage of the region. |
| [`regionBottom`](auxiliary-RegionDefinition.md#regionbottom) | *NSInteger* | The Bottom-most coordinate or percentage of the region. |
| [`regionMeasuredByPercentage`](auxiliary-RegionDefinition.md#regionmeasuredbypercentage) | *NSInteger* | Sets whether or not to use percentage to measure the region size. |

## regionTop

The top-most coordinate or percentage of the region.

```objc
NSInteger regionTop
```

**Value range**
regionMeasuredByPercentage = 0: [0, 0x7fffffff]  
regionMeasuredByPercentage = 1: [0, 100]  

**Default value**
0

## regionLeft

The left-most coordinate or percentage of the region.

```objc
NSInteger regionLeft
```

**Value range**
regionMeasuredByPercentage = 0: [0, 0x7fffffff]  
regionMeasuredByPercentage = 1: [0, 100]  

**Default value**
0

## regionRight

The right-most coordinate or percentage of the region.

```objc
NSInteger regionRight
```

**Value range**
regionMeasuredByPercentage = 0: [0, 0x7fffffff]
regionMeasuredByPercentage = 1: [0, 100]

**Default value**
0

## regionBottom

The bottom-most coordinate or percentage of the region.

```objc
NSInteger regionBottom
```

**Value range**
regionMeasuredByPercentage = 0: [0, 0x7fffffff]  
regionMeasuredByPercentage = 1: [0, 100]  

**Default value**
0

## regionMeasuredByPercentage

Sets whether or not to use percentage to measure the region size.

```objc
NSInteger regionMeasuredByPercentage
```

**Value range**
[0, 1]

**Default value**
0

**Remarks**
When it's set to 1, the values of Top, Left, Right, Bottom indicate percentage (from 0 to 100); Otherwise, they indicate coordinates. 0: not by percentage 1: by percentage.
