# AWS::MediaPackage::PackagingConfiguration CmafEncryption<a name="aws-properties-mediapackage-packagingconfiguration-cmafencryption"></a>

Holds encryption information so that access to the content can be controlled by a DRM solution\.

## Syntax<a name="aws-properties-mediapackage-packagingconfiguration-cmafencryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-packagingconfiguration-cmafencryption-syntax.json"></a>

```
{
  "[SpekeKeyProvider](#cfn-mediapackage-packagingconfiguration-cmafencryption-spekekeyprovider)" : 
}
```

### YAML<a name="aws-properties-mediapackage-packagingconfiguration-cmafencryption-syntax.yaml"></a>

```
  [SpekeKeyProvider](#cfn-mediapackage-packagingconfiguration-cmafencryption-spekekeyprovider): 
```

## Properties<a name="aws-properties-mediapackage-packagingconfiguration-cmafencryption-properties"></a>

`SpekeKeyProvider`  <a name="cfn-mediapackage-packagingconfiguration-cmafencryption-spekekeyprovider"></a>
Parameters for the SPEKE key provider\.  
*Required*: Yes  
*Type*:   
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)