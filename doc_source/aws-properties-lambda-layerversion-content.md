# AWS::Lambda::LayerVersion Content<a name="aws-properties-lambda-layerversion-content"></a>

A ZIP archive that contains the contents of an [AWS Lambda layer](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html)\.

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
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `^[0-9A-Za-z\.\-_]*(?<!\.)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3Key`  <a name="cfn-lambda-layerversion-content-s3key"></a>
The Amazon S3 key of the layer archive\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3ObjectVersion`  <a name="cfn-lambda-layerversion-content-s3objectversion"></a>
For versioned objects, the version of the layer archive object to use\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)