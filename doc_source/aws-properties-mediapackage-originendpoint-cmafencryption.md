# AWS::MediaPackage::OriginEndpoint CmafEncryption<a name="aws-properties-mediapackage-originendpoint-cmafencryption"></a>

Holds encryption information so that access to the content can be controlled by a DRM solution\. 

## Syntax<a name="aws-properties-mediapackage-originendpoint-cmafencryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-originendpoint-cmafencryption-syntax.json"></a>

```
{
  "[KeyRotationIntervalSeconds](#cfn-mediapackage-originendpoint-cmafencryption-keyrotationintervalseconds)" : Integer,
  "[SpekeKeyProvider](#cfn-mediapackage-originendpoint-cmafencryption-spekekeyprovider)" : SpekeKeyProvider
}
```

### YAML<a name="aws-properties-mediapackage-originendpoint-cmafencryption-syntax.yaml"></a>

```
  [KeyRotationIntervalSeconds](#cfn-mediapackage-originendpoint-cmafencryption-keyrotationintervalseconds): Integer
  [SpekeKeyProvider](#cfn-mediapackage-originendpoint-cmafencryption-spekekeyprovider): 
    SpekeKeyProvider
```

## Properties<a name="aws-properties-mediapackage-originendpoint-cmafencryption-properties"></a>

`KeyRotationIntervalSeconds`  <a name="cfn-mediapackage-originendpoint-cmafencryption-keyrotationintervalseconds"></a>
Number of seconds before AWS Elemental MediaPackage rotates to a new key\. By default, rotation is set to 60 seconds\. Set to `0` to disable key rotation\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpekeKeyProvider`  <a name="cfn-mediapackage-originendpoint-cmafencryption-spekekeyprovider"></a>
Parameters for the SPEKE key provider\.  
*Required*: Yes  
*Type*: [SpekeKeyProvider](aws-properties-mediapackage-originendpoint-spekekeyprovider.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)