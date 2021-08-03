---
layout: default-layout
title: Dynamsoft Barcode Reader Android API Reference - Camera Methods
description: This page shows Camera methods of Dynamsoft Barcode Reader for Android SDK.
keywords: Camera methods, BarcodeReader, api reference, android
needAutoGenerateSidebar: true
noTitleIndex: true
---


# Camera Methods

| Method | Description |
|--------|-------------|
| [`StartCameraEnhancer`](#startcameraenhancer) | Start using Dynamsoft Camera Enhancer |
| [`StopCameraEnhancer`](#stopcameraenhancer) | Stop using Dynamsoft Camera Enhancer |
| [`PauseCameraEnhancer`](#pausecameraenhancer) | Pause the process of Dynamsoft Camera Enhancer |
| [`ResumeCameraEnhancer`](#resumecameraenhancer) | Pause the process of Dynamsoft Camera Enhancer |
| [`SetCameraEnhancerParam`](#setcameraenhancerparam) | Set the parameters for Dynamsoft Camera Enhancer in Barcode reader |

This page illustrates the controlling of `Dynamsoft Camera Enhancer`. To get a better understanding of this section, please read more about [`Dynamsoft Camera Enhancer`](https://www.dynamsoft.com/camera-enhancer/docs/introduction/?ver=latest).

## StartCameraEnhancer

APIs that controlling the start of `Dynamsoft Camera Enhancer`.

```java
void com.dynamsoft.dbr.BarcodeReader.StartCameraEnhancer()
```

**Code Snippet**

```java
    reader.StartCameraEnhancer();
```

## StopCameraEnhancer

APIs that controlling the start of `Dynamsoft Camera Enhancer`.

```java
void com.dynamsoft.dbr.BarcodeReader.StopCameraEnhancer()
```

**Code Snippet**

```java
    reader.StopCameraEnhancer();
```

## PauseCameraEnhancer

APIs that controlling the pause of `Dynamsoft Camera Enhancer`.

```java
void com.dynamsoft.dbr.BarcodeReader.PauseCameraEnhancer()
```

**Code Snippet**

```java
reader.PauseCameraEnhancer();
```

## ResumeCameraEnhancer

APIs that controlling the resume of `Dynamsoft Camera Enhancer`.

```java
void com.dynamsoft.dbr.BarcodeReader.ResumeCameraEnhancer()
```

**Code Snippet**

```java
reader.ResumeCameraEnhancer();
```

## SetCameraEnhancerParam

Set the CameraEnhancer parameters.

```java
void com.dynamsoft.dbr.BarcodeReader.ResumeCameraEnhancer()
```

**Parameters**

`cameraInstance`: The instance of Dynamsoft Camera Enhancer.  
[`textResultCallback`](interface.md#textresultcallback): The text result callback.  
[`intermediateResultCallback`](interface.md#intermediateresultcallback): The intermediate result callback.

**Exceptions**

[`BarcodeReaderException`](auxiliary-BarcodeReaderException.md)

**Code Snippet**

```java
    DCESettingParameters dceSettingParameters = new DCESettingParameters();
    dceSettingParameters._cameraInstance = mCameraEnhancer;
    dceSettingParameters._textResultCallback = mTextResultCallback;
    dceSettingParameters._irtCallback = mIntermediateResultCallback;
    reader.SetCameraEnhancerParam(dceSettingParameters);
```

**See Also**

[`DCESettingParameters`](auxiliary-DCESettingParameters.md): The parameters that will be used in `SetCameraEnhancerParam`.
