# AWS::MediaPackage::OriginEndpoint DashEncryption<a name="aws-properties-mediapackage-originendpoint-dashencryption"></a>

Holds encryption information so that access to the content can be controlled by a DRM solution\. 

## Syntax<a name="aws-properties-mediapackage-originendpoint-dashencryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-originendpoint-dashencryption-syntax.json"></a>

```
{
  "[KeyRotationIntervalSeconds](#cfn-mediapackage-originendpoint-dashencryption-keyrotationintervalseconds)" : Integer,
  "[SpekeKeyProvider](#cfn-mediapackage-originendpoint-dashencryption-spekekeyprovider)" : SpekeKeyProvider
}
```

### YAML<a name="aws-properties-mediapackage-originendpoint-dashencryption-syntax.yaml"></a>

```
  [KeyRotationIntervalSeconds](#cfn-mediapackage-originendpoint-dashencryption-keyrotationintervalseconds): Integer
  [SpekeKeyProvider](#cfn-mediapackage-originendpoint-dashencryption-spekekeyprovider): 
    SpekeKeyProvider
```

## Properties<a name="aws-properties-mediapackage-originendpoint-dashencryption-properties"></a>

`KeyRotationIntervalSeconds`  <a name="cfn-mediapackage-originendpoint-dashencryption-keyrotationintervalseconds"></a>
Number of seconds before AWS Elemental MediaPackage rotates to a new key\. By default, rotation is set to 60 seconds\. Set to `0` to disable key rotation\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpekeKeyProvider`  <a name="cfn-mediapackage-originendpoint-dashencryption-spekekeyprovider"></a>
Parameters for the SPEKE key provider\.  
*Required*: Yes  
*Type*: [SpekeKeyProvider](aws-properties-mediapackage-originendpoint-spekekeyprovider.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)