# AWS::MediaPackage::OriginEndpoint MssEncryption<a name="aws-properties-mediapackage-originendpoint-mssencryption"></a>

Holds encryption information so that access to the content can be controlled by a DRM solution\. 

## Syntax<a name="aws-properties-mediapackage-originendpoint-mssencryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-originendpoint-mssencryption-syntax.json"></a>

```
{
  "[SpekeKeyProvider](#cfn-mediapackage-originendpoint-mssencryption-spekekeyprovider)" : SpekeKeyProvider
}
```

### YAML<a name="aws-properties-mediapackage-originendpoint-mssencryption-syntax.yaml"></a>

```
  [SpekeKeyProvider](#cfn-mediapackage-originendpoint-mssencryption-spekekeyprovider): 
    SpekeKeyProvider
```

## Properties<a name="aws-properties-mediapackage-originendpoint-mssencryption-properties"></a>

`SpekeKeyProvider`  <a name="cfn-mediapackage-originendpoint-mssencryption-spekekeyprovider"></a>
Parameters for the SPEKE key provider\.  
*Required*: Yes  
*Type*: [SpekeKeyProvider](aws-properties-mediapackage-originendpoint-spekekeyprovider.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)