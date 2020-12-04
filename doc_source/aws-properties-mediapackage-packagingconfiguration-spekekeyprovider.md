# AWS::MediaPackage::PackagingConfiguration SpekeKeyProvider<a name="aws-properties-mediapackage-packagingconfiguration-spekekeyprovider"></a>

A configuration for accessing an external Secure Packager and Encoder Key Exchange \(SPEKE\) service that provides encryption keys\.

## Syntax<a name="aws-properties-mediapackage-packagingconfiguration-spekekeyprovider-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-packagingconfiguration-spekekeyprovider-syntax.json"></a>

```
{
  "[RoleArn](#cfn-mediapackage-packagingconfiguration-spekekeyprovider-rolearn)" : String,
  "[SystemIds](#cfn-mediapackage-packagingconfiguration-spekekeyprovider-systemids)" : [ String, ... ],
  "[Url](#cfn-mediapackage-packagingconfiguration-spekekeyprovider-url)" : String
}
```

### YAML<a name="aws-properties-mediapackage-packagingconfiguration-spekekeyprovider-syntax.yaml"></a>

```
  [RoleArn](#cfn-mediapackage-packagingconfiguration-spekekeyprovider-rolearn): String
  [SystemIds](#cfn-mediapackage-packagingconfiguration-spekekeyprovider-systemids): 
    - String
  [Url](#cfn-mediapackage-packagingconfiguration-spekekeyprovider-url): String
```

## Properties<a name="aws-properties-mediapackage-packagingconfiguration-spekekeyprovider-properties"></a>

`RoleArn`  <a name="cfn-mediapackage-packagingconfiguration-spekekeyprovider-rolearn"></a>
The ARN for the IAM role that's granted by the key provider to provide access to the key provider API\. Valid format: arn:aws:iam::\{accountID\}:role/\{name\}   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SystemIds`  <a name="cfn-mediapackage-packagingconfiguration-spekekeyprovider-systemids"></a>
List of unique identifiers for the DRM systems to use, as defined in the CPIX specification\.   
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-mediapackage-packagingconfiguration-spekekeyprovider-url"></a>
URL for the key provider's key retrieval API endpoint\. Must start with https://\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)