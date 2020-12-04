# AWS::MediaPackage::OriginEndpoint HlsEncryption<a name="aws-properties-mediapackage-originendpoint-hlsencryption"></a>

Holds encryption information so that access to the content can be controlled by a DRM solution\. 

## Syntax<a name="aws-properties-mediapackage-originendpoint-hlsencryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-originendpoint-hlsencryption-syntax.json"></a>

```
{
  "[ConstantInitializationVector](#cfn-mediapackage-originendpoint-hlsencryption-constantinitializationvector)" : String,
  "[EncryptionMethod](#cfn-mediapackage-originendpoint-hlsencryption-encryptionmethod)" : String,
  "[KeyRotationIntervalSeconds](#cfn-mediapackage-originendpoint-hlsencryption-keyrotationintervalseconds)" : Integer,
  "[RepeatExtXKey](#cfn-mediapackage-originendpoint-hlsencryption-repeatextxkey)" : Boolean,
  "[SpekeKeyProvider](#cfn-mediapackage-originendpoint-hlsencryption-spekekeyprovider)" : SpekeKeyProvider
}
```

### YAML<a name="aws-properties-mediapackage-originendpoint-hlsencryption-syntax.yaml"></a>

```
  [ConstantInitializationVector](#cfn-mediapackage-originendpoint-hlsencryption-constantinitializationvector): String
  [EncryptionMethod](#cfn-mediapackage-originendpoint-hlsencryption-encryptionmethod): String
  [KeyRotationIntervalSeconds](#cfn-mediapackage-originendpoint-hlsencryption-keyrotationintervalseconds): Integer
  [RepeatExtXKey](#cfn-mediapackage-originendpoint-hlsencryption-repeatextxkey): Boolean
  [SpekeKeyProvider](#cfn-mediapackage-originendpoint-hlsencryption-spekekeyprovider): 
    SpekeKeyProvider
```

## Properties<a name="aws-properties-mediapackage-originendpoint-hlsencryption-properties"></a>

`ConstantInitializationVector`  <a name="cfn-mediapackage-originendpoint-hlsencryption-constantinitializationvector"></a>
A 128\-bit, 16\-byte hex value represented by a 32\-character string, used with the key for encrypting blocks\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionMethod`  <a name="cfn-mediapackage-originendpoint-hlsencryption-encryptionmethod"></a>
HLS encryption type\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyRotationIntervalSeconds`  <a name="cfn-mediapackage-originendpoint-hlsencryption-keyrotationintervalseconds"></a>
Number of seconds before AWS Elemental MediaPackage rotates to a new key\. By default, rotation is set to 60 seconds\. Set to `0` to disable key rotation\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RepeatExtXKey`  <a name="cfn-mediapackage-originendpoint-hlsencryption-repeatextxkey"></a>
Repeat the `EXT-X-KEY `directive for every media segment\. This might result in an increase in client requests to the DRM server\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpekeKeyProvider`  <a name="cfn-mediapackage-originendpoint-hlsencryption-spekekeyprovider"></a>
Parameters for the SPEKE key provider\.  
*Required*: Yes  
*Type*: [SpekeKeyProvider](aws-properties-mediapackage-originendpoint-spekekeyprovider.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)