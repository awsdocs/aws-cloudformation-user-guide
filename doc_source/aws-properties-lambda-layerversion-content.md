# AWS Lambda LayerVersion Content<a name="aws-properties-lambda-layerversion-content"></a>

<a name="aws-properties-lambda-layerversion-content-description"></a>The `Content` property type specifies the ZIP archive for an AWS Lambda layer version\.

<a name="aws-properties-lambda-layerversion-content-inheritance"></a> `Content` is a property of the [AWS::Lambda::LayerVersion](aws-resource-lambda-layerversion.md) resource\.

## Syntax<a name="aws-properties-lambda-layerversion-content-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-layerversion-content-syntax.json"></a>

```
{
  "[S3Bucket](#cfn-lambda-layerversion-content-s3bucket)" : String,
  "[S3Key](#cfn-lambda-layerversion-content-s3key)" : String,
  "[S3ObjectVersion](#cfn-lambda-layerversion-content-s3objectversion)" : String
}
```

### YAML<a name="aws-properties-lambda-layerversion-content-syntax.yaml"></a>

```
[S3Bucket](#cfn-lambda-layerversion-content-s3bucket): String
[S3Key](#cfn-lambda-layerversion-content-s3key): String
[S3ObjectVersion](#cfn-lambda-layerversion-content-s3objectversion): String
```

## Properties<a name="aws-properties-lambda-layerversion-content-properties"></a>

`S3Bucket`  <a name="cfn-lambda-layerversion-content-s3bucket"></a>
The Amazon S3 bucket of the layer archive\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`S3Key`  <a name="cfn-lambda-layerversion-content-s3key"></a>
The Amazon S3 key of the layer archive\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`S3ObjectVersion`  <a name="cfn-lambda-layerversion-content-s3objectversion"></a>
For versioned objects, the version of the layer archive object to use\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-lambda-layerversion-content-seealso"></a>
+ [LayerVersionContentInput](https://docs.aws.amazon.com/lambda/latest/dg/API_LayerVersionContentInput.html) in the *AWS Lambda Developer Guide*