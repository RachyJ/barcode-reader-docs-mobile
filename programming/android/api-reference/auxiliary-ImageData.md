---
layout: default-layout
title: Dynamsoft Barcode Reader Android API Reference - ImageData Class
description: This page shows the ImageData Class of Dynamsoft Barcode Reader for Android SDK.
keywords: ImageData, class, api reference, android
needAutoGenerateSidebar: true
needGenerateH3Content: true
---


# ImageData

Stores the image data.  

## Attributes

| Attribute | Type |
|---------- | ---- |
| [`bytes`](#bytes) | *byte\[\]* |
| [`width`](#width) | *int* |
| [`height`](#height) | *int* |
| [`stride`](#stride) | *int* |
| [`format`](#format) | *int* |

### bytes

The image data content in a byte array.

```java
byte[] com.dynamsoft.dbr.ImageData.bytes
```

### width

The width of the image in pixels.  

```java
int com.dynamsoft.dbr.ImageData.width
```

### height

The height of the image in pixels.

```java
int com.dynamsoft.dbr.ImageData.height
```

### stride

The stride (or scan width) of the image.

```java
int com.dynamsoft.dbr.ImageData.stride
```

### format

The image pixel format used in the image byte array.

```java
int com.dynamsoft.dbr.ImageData.format
```