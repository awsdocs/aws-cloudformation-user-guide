# AWS::MediaPackage::PackagingConfiguration HlsEncryption<a name="aws-properties-mediapackage-packagingconfiguration-hlsencryption"></a>

Holds encryption information so that access to the content can be controlled by a DRM solution\.

## Syntax<a name="aws-properties-mediapackage-packagingconfiguration-hlsencryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-packagingconfiguration-hlsencryption-syntax.json"></a>

```
{
  "[ConstantInitializationVector](#cfn-mediapackage-packagingconfiguration-hlsencryption-constantinitializationvector)" : String,
  "[EncryptionMethod](#cfn-mediapackage-packagingconfiguration-hlsencryption-encryptionmethod)" : String,
  "[SpekeKeyProvider](#cfn-mediapackage-packagingconfiguration-hlsencryption-spekekeyprovider)" : 
}
```

### YAML<a name="aws-properties-mediapackage-packagingconfiguration-hlsencryption-syntax.yaml"></a>

```
  [ConstantInitializationVector](#cfn-mediapackage-packagingconfiguration-hlsencryption-constantinitializationvector): String
  [EncryptionMethod](#cfn-mediapackage-packagingconfiguration-hlsencryption-encryptionmethod): String
  [SpekeKeyProvider](#cfn-mediapackage-packagingconfiguration-hlsencryption-spekekeyprovider):
```

## Properties<a name="aws-properties-mediapackage-packagingconfiguration-hlsencryption-properties"></a>

`ConstantInitializationVector`  <a name="cfn-mediapackage-packagingconfiguration-hlsencryption-constantinitializationvector"></a>
A 128\-bit, 16\-byte hex value represented by a 32\-character string, used with the key for encrypting blocks\. If you don't specify a constant initialization vector \(IV\), MediaPackage periodically rotates the IV\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionMethod`  <a name="cfn-mediapackage-packagingconfiguration-hlsencryption-encryptionmethod"></a>
HLS encryption type\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpekeKeyProvider`  <a name="cfn-mediapackage-packagingconfiguration-hlsencryption-spekekeyprovider"></a>
Parameters for the SPEKE key provider\.  
*Required*: Yes  
*Type*:   
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)