# AWS::MediaPackageV2::OriginEndpoint Encryption<a name="aws-properties-mediapackagev2-originendpoint-encryption"></a>

A collection of video encryption presets\.

Value description: 
+  `PRESET-VIDEO-1` \- Use one content key to encrypt all of the video tracks in your stream\.
+  `PRESET-VIDEO-2` \- Use one content key to encrypt all of the SD video tracks and one content key for all HD and higher resolutions video tracks\.
+  `PRESET-VIDEO-3` \- Use one content key to encrypt all of the SD video tracks, one content key for HD video tracks and one content key for all UHD video tracks\.
+  `PRESET-VIDEO-4` \- Use one content key to encrypt all of the SD video tracks, one content key for HD video tracks, one content key for all UHD1 video tracks and one content key for all UHD2 video tracks\.
+  `PRESET-VIDEO-5` \- Use one content key to encrypt all of the SD video tracks, one content key for HD1 video tracks, one content key for HD2 video tracks, one content key for all UHD1 video tracks and one content key for all UHD2 video tracks\.
+  `PRESET-VIDEO-6` \- Use one content key to encrypt all of the SD video tracks, one content key for HD1 video tracks, one content key for HD2 video tracks and one content key for all UHD video tracks\.
+  `PRESET-VIDEO-7` \- Use one content key to encrypt all of the SD\+HD1 video tracks, one content key for HD2 video tracks and one content key for all UHD video tracks\.
+  `PRESET-VIDEO-8` \- Use one content key to encrypt all of the SD\+HD1 video tracks, one content key for HD2 video tracks, one content key for all UHD1 video tracks and one content key for all UHD2 video tracks\.
+  `SHARED` \- Use the same content key for all of the video and audio tracks in your stream\.
+  `UNENCRYPTED` \- Don't encrypt any of the video tracks in your stream\.

## Syntax<a name="aws-properties-mediapackagev2-originendpoint-encryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackagev2-originendpoint-encryption-syntax.json"></a>

```
{
  "[ConstantInitializationVector](#cfn-mediapackagev2-originendpoint-encryption-constantinitializationvector)" : String,
  "[EncryptionMethod](#cfn-mediapackagev2-originendpoint-encryption-encryptionmethod)" : EncryptionMethod,
  "[KeyRotationIntervalSeconds](#cfn-mediapackagev2-originendpoint-encryption-keyrotationintervalseconds)" : Integer,
  "[SpekeKeyProvider](#cfn-mediapackagev2-originendpoint-encryption-spekekeyprovider)" : SpekeKeyProvider
}
```

### YAML<a name="aws-properties-mediapackagev2-originendpoint-encryption-syntax.yaml"></a>

```
  [ConstantInitializationVector](#cfn-mediapackagev2-originendpoint-encryption-constantinitializationvector): String
  [EncryptionMethod](#cfn-mediapackagev2-originendpoint-encryption-encryptionmethod): 
    EncryptionMethod
  [KeyRotationIntervalSeconds](#cfn-mediapackagev2-originendpoint-encryption-keyrotationintervalseconds): Integer
  [SpekeKeyProvider](#cfn-mediapackagev2-originendpoint-encryption-spekekeyprovider): 
    SpekeKeyProvider
```

## Properties<a name="aws-properties-mediapackagev2-originendpoint-encryption-properties"></a>

`ConstantInitializationVector`  <a name="cfn-mediapackagev2-originendpoint-encryption-constantinitializationvector"></a>
A 128\-bit, 16\-byte hex value represented by a 32\-character string, used in conjunction with the key for encrypting content\. If you don't specify a value, then MediaPackage creates the constant initialization vector \(IV\)\.  
*Required*: No  
*Type*: String  
*Minimum*: `32`  
*Maximum*: `32`  
*Pattern*: `[0-9a-fA-F]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionMethod`  <a name="cfn-mediapackagev2-originendpoint-encryption-encryptionmethod"></a>
The encryption method to use\.  
*Required*: Yes  
*Type*: [EncryptionMethod](aws-properties-mediapackagev2-originendpoint-encryptionmethod.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyRotationIntervalSeconds`  <a name="cfn-mediapackagev2-originendpoint-encryption-keyrotationintervalseconds"></a>
The interval, in seconds, to rotate encryption keys for the origin endpoint\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `300`  
*Maximum*: `31536000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpekeKeyProvider`  <a name="cfn-mediapackagev2-originendpoint-encryption-spekekeyprovider"></a>
The SPEKE key provider to use for encryption\.  
*Required*: Yes  
*Type*: [SpekeKeyProvider](aws-properties-mediapackagev2-originendpoint-spekekeyprovider.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)