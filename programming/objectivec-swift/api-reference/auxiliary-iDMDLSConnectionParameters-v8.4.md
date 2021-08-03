---
layout: default-layout
title: Dynamsoft Barcode Reader Objective-C & Swift API Reference - iDMLTSConnectionParameters Class
description: This page shows the iDMLTSConnectionParameters Class of Dynamsoft Barcode Reader for iOS SDK.
keywords: iDMLTSConnectionParameters, class, api reference, objective-c, oc, swift
needAutoGenerateSidebar: true
noTitleIndex: true
---


# Class iDMLTSConnectionParameters

Defines a struct to configure the parameters to connect to the license server.  

| Attribute | Type | Descriptions |
|---------- | ---- | ------------ |
| [`mainServerURL`](#mainserverurl) | *NSString\** | The URL of the license tracking server. |
| [`standbyServerURL`](#standbyserverurl) | *NSString\** | The URL of the standby license tracking server. |
| [`handshakeCode`](#handshakecode) | *NSString\** | The handshake code. |
| [`sessionPassword`](#sessionpassword) | *NSString\** | The session password of the handshake code set in license tracking server. |
| [`chargeWay`](#chargeway) | *EnumDMChargeWay* | Sets the charge way. |
| [`UUIDGenerationMethod`](#uuidgenerationmethod) | *EnumDMUUIDGenerationMethod* | Sets the method to generate UUID. |
| [`maxBufferDays`](#maxbufferdays) | *NSInteger* | Sets the max days to buffer the license info. |
| [`limitedLicenseModules`](#limitedlicensemodules) | *NSArray\** | Sets the license modules to use. |
| [`organizationID`](#organizationid) | *NSString\** | The organization ID got from Dynamsoft. |

## mainServerURL

The URL of the license tracking server.

```objc
NSString* mainServerURL
```

**Value range**
Any string value

**Default value**
nil

**Remarks**
If you choose "Dynamsoft-hosting", then no need to change the value of MainServerURL and StandbyServerURL. When both are set to nil (default value), it will connect to Dynamsoft's license tracking servers for online verification.

## standbyServerURL

The URL of the standby license tracking server.

```objc
NSString* standbyServerURL
```

**Value range**
Any string value

**Default value**
nil

**Remarks**
If you choose "Dynamsoft-hosting", then no need to change the value of MainServerURL and StandbyServerURL. When both are set to nil (default value), it will connect to Dynamsoft's license tracking servers for online verification.

## handshakeCode

The handshake code.

```objc
NSString* handshakeCode
```

**Value range**
Any string value

**Default value**
nil

## sessionPassword

The session password of the handshake code set in license tracking server.

```objc
NSString* sessionPassword
```

**Value range**
Any string value

**Default value**
nil

## chargeWay

Sets the charge way.

```objc
EnumDMChargeWay chargeWay
```

**Value range**
Any one of the [`EnumDMChargeWay`]({{ site.enumerations }}other-enums.html#dm_chargeWay) Enumeration items.

**Default value**
EnumDMChargeWayAuto

**See also**  
[`EnumDMChargeWay`]({{ site.enumerations }}other-enums.html#dm_chargeWay)

## UUIDGenerationMethod

Sets the method to generate UUID.

```objc
EnumDMUUIDGenerationMethod UUIDGenerationMethod
```

**Value range**
Any one of the [`EnumDMUUIDGenerationMethod`]({{ site.enumerations }}other-enums.html#dm_uuidgenerationmethod) Enumeration items.

**Default value**
EnumDMUUIDGenerationMethodRandom

**See also**  
[`EnumDMUUIDGenerationMethod`]({{ site.enumerations }}other-enums.html#dm_uuidgenerationmethod)

## maxBufferDays

Sets the max days to buffer the license info.

```objc
NSInteger maxBufferDays
```

**Value range**
[7,0x7fffffff]

**Default value**
7

## limitedLicenseModules

Sets the license modules to use.

```objc
NSArray* limitedLicenseModules
```

**Value range**
Each array item can be any one of the [`EnumDMLicenseModule`]({{ site.enumerations }}other-enums.html#dm_licensemodule) Enumeration items.

**Default value**
nil

**See also**  
[`EnumDMLicenseModule`]({{ site.enumerations }}other-enums.html#dm_licensemodule)

## organizationID

The organization ID got from Dynamsoft.

```objc
NSString* organizationID
```

**Value range**
Any string value

**Default value**
""
