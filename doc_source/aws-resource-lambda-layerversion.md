# AWS::Lambda::LayerVersion<a name="aws-resource-lambda-layerversion"></a>

The `AWS::Lambda::LayerVersion` resource creates a layer version in AWS Lambda\. For more information, see [AWS Lambda Layers](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html) in the *AWS Lambda Developer Guide*\.

## Syntax<a name="aws-resource-lambda-layerversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lambda-layerversion-syntax.json"></a>

```
{
  "Type" : "AWS::Lambda::LayerVersion",
  "Properties" : {
    "[CompatibleRuntimes](#cfn-lambda-layerversion-compatibleruntimes)" : [ String, ... ],
    "[Content](#cfn-lambda-layerversion-content)" : [*Content*](aws-properties-lambda-layerversion-content.md),
    "[Description](#cfn-lambda-layerversion-description)" : String,
    "[LayerName](#cfn-lambda-layerversion-layername)" : String,
    "[LicenseInfo](#cfn-lambda-layerversion-licenseinfo)" : String  
  }
}
```

### YAML<a name="aws-resource-lambda-layerversion-syntax.yaml"></a>

```
Type: "AWS::Lambda::LayerVersion"
Properties:
  [CompatibleRuntimes](#cfn-lambda-layerversion-compatibleruntimes): 
    - String
    - ...
  [Content](#cfn-lambda-layerversion-content): 
    [*Content*](aws-properties-lambda-layerversion-content.md)
  [Description](#cfn-lambda-layerversion-description): String
  [LayerName](#cfn-lambda-layerversion-layername): String
  [LicenseInfo](#cfn-lambda-layerversion-licenseinfo): String
```

## Properties<a name="aws-resource-lambda-layerversion-properties"></a>

`CompatibleRuntimes`  <a name="cfn-lambda-layerversion-compatibleruntimes"></a>
A list of compatible [function runtimes](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html)\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Content`  <a name="cfn-lambda-layerversion-content"></a>
The function layer archive\.  
 *Required*: Yes  
 *Type*: [Content](aws-properties-lambda-layerversion-content.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Description`  <a name="cfn-lambda-layerversion-description"></a>
The description of the version\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`LayerName`  <a name="cfn-lambda-layerversion-layername"></a>
The name of the layer\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`LicenseInfo`  <a name="cfn-lambda-layerversion-licenseinfo"></a>
The layer's software license\. It can be either of the following:  
+ An [SPDX license identifier](https://spdx.org/licenses/)\. For example, `MIT`\.
+ The URL of a license hosted on the internet\. For example, `https://opensource.org/licenses/MIT`\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-lambda-layerversion-returnvalues"></a>

### Ref<a name="aws-resource-lambda-layerversion-ref"></a>

When you pass the logical ID of an `AWS::Lambda::LayerVersion` resource to the intrinsic `Ref` function, the function returns the ARN of the layer version, such as `arn:aws:lambda:us-west-2:123456789012:layer:my-layer:1`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-lambda-layerversion-examples"></a>

### Create a Layer Version<a name="aws-resource-lambda-layerversion-example1"></a>

The following example creates a layer version from a ZIP file stored in Amazon S3\.

#### JSON<a name="aws-resource-lambda-layerversion-example1.json"></a>

```
{
  "Type" : "AWS::Lambda::LayerVersion",
  "Properties" : {
    "CompatibleRuntimes" : [ "python3.6", "python3.7" ],
    "Content" : {
      "S3Bucket" : "my-bucket-us-west-2-123456789012",
      "S3Key" : "layer.zip"
    },
    "Description" : "My layer",
    "LayerName" : "my-layer",
    "LicenseInfo" : "MIT"
  }
}
```

#### YAML<a name="aws-resource-lambda-layerversion-example1.yaml"></a>

```
Type: "AWS::Lambda::LayerVersion"
Properties:
  CompatibleRuntimes: 
    - python3.6
    - python3.7
  Content: 
    S3Bucket: my-bucket-us-west-2-123456789012
    S3Key: layer.zip
  Description: My layer
  LayerName: my-layer
  LicenseInfo: MIT
```

## See Also<a name="aws-resource-lambda-layerversion-seealso"></a>
+ [PublishLayerVersion](https://docs.aws.amazon.com/lambda/latest/dg/API_PublishLayerVersion.html) in the *AWS Lambda Developer Guide*