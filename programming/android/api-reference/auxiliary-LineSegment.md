---
layout: default-layout
title: Dynamsoft Barcode Reader Android API Reference - LineSegment Class
description: This page shows the LineSegment Class of Dynamsoft Barcode Reader for Android SDK.
keywords: LineSegment, class, api reference, android
needAutoGenerateSidebar: true
needGenerateH3Content: true
---


# Class LineSegment

Stores line segment data.

| Attribute | Type | Descriptions |
|---------- | ---- | ----------- |
| [`startPoint`](#startpoint) | [`Point`](auxiliary-Point.md) | The start point of the line segment. |
| [`endPoint`](#endpoint) | [`Point`](auxiliary-Point.md) | The end point of the line segment. |
| [`linesConfidenceCoefficients`](#linesconfidencecoefficients) | *byte\[\]* | The confidence coefficients for lines. |

## startPoint

The start point of the line segment.

```java
Point[] startPoint
```

## endPoint

The end point of the line segment.

```java
Point[] endPoint
```

## linesConfidenceCoefficients

The confidence coefficients for lines. There are 4 coefficients in this set:  

1. linesConfidenceCoefficients\[0\] is average positive amplitude;
2. linesConfidenceCoefficients\[1\] is max positive amplitude;
3. linesConfidenceCoefficients\[2\] is average negative amplitude;
4. linesConfidenceCoefficients\[3\] is max negative amplitude.

```java
byte[] linesConfidenceCoefficients
```
