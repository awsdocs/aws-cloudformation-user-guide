# AWS::MediaPackage::PackagingConfiguration MssEncryption<a name="aws-properties-mediapackage-packagingconfiguration-mssencryption"></a>

Holds encryption information so that access to the content can be controlled by a DRM solution\.

## Syntax<a name="aws-properties-mediapackage-packagingconfiguration-mssencryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-packagingconfiguration-mssencryption-syntax.json"></a>

```
{
  "[SpekeKeyProvider](#cfn-mediapackage-packagingconfiguration-mssencryption-spekekeyprovider)" : 
}
```

### YAML<a name="aws-properties-mediapackage-packagingconfiguration-mssencryption-syntax.yaml"></a>

```
  [SpekeKeyProvider](#cfn-mediapackage-packagingconfiguration-mssencryption-spekekeyprovider): 
```

## Properties<a name="aws-properties-mediapackage-packagingconfiguration-mssencryption-properties"></a>

`SpekeKeyProvider`  <a name="cfn-mediapackage-packagingconfiguration-mssencryption-spekekeyprovider"></a>
Parameters for the SPEKE key provider\.  
*Required*: Yes  
*Type*:   
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)