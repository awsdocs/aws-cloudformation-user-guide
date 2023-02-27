# AWS::S3ObjectLambda::AccessPoint TransformationConfiguration<a name="aws-properties-s3objectlambda-accesspoint-transformationconfiguration"></a>

A configuration used when creating an Object Lambda Access Point transformation\.

## Syntax<a name="aws-properties-s3objectlambda-accesspoint-transformationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3objectlambda-accesspoint-transformationconfiguration-syntax.json"></a>

```
{
  "[Actions](#cfn-s3objectlambda-accesspoint-transformationconfiguration-actions)" : [ String, ... ],
  "[ContentTransformation](#cfn-s3objectlambda-accesspoint-transformationconfiguration-contenttransformation)" : ContentTransformation
}
```

### YAML<a name="aws-properties-s3objectlambda-accesspoint-transformationconfiguration-syntax.yaml"></a>

```
  [Actions](#cfn-s3objectlambda-accesspoint-transformationconfiguration-actions): 
    - String
  [ContentTransformation](#cfn-s3objectlambda-accesspoint-transformationconfiguration-contenttransformation): 
    ContentTransformation
```

## Properties<a name="aws-properties-s3objectlambda-accesspoint-transformationconfiguration-properties"></a>

`Actions`  <a name="cfn-s3objectlambda-accesspoint-transformationconfiguration-actions"></a>
A container for the action of an Object Lambda Access Point configuration\. Valid inputs are `GetObject`, `HeadObject`, `ListObject`, and `ListObjectV2`\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContentTransformation`  <a name="cfn-s3objectlambda-accesspoint-transformationconfiguration-contenttransformation"></a>
A container for the content transformation of an Object Lambda Access Point configuration\. Can include the FunctionArn and FunctionPayload\. For more information, see [AwsLambdaTransformation](https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_AwsLambdaTransformation.html) in the *Amazon S3 API Reference*\.  
*Required*: Yes  
*Type*: [ContentTransformation](aws-properties-s3objectlambda-accesspoint-contenttransformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)