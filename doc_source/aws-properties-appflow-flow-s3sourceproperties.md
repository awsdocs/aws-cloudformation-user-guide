# AWS::AppFlow::Flow S3SourceProperties<a name="aws-properties-appflow-flow-s3sourceproperties"></a>

 The properties that are applied when Amazon S3 is being used as the flow source\. 

## Syntax<a name="aws-properties-appflow-flow-s3sourceproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-s3sourceproperties-syntax.json"></a>

```
{
  "[BucketName](#cfn-appflow-flow-s3sourceproperties-bucketname)" : String,
  "[BucketPrefix](#cfn-appflow-flow-s3sourceproperties-bucketprefix)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-s3sourceproperties-syntax.yaml"></a>

```
  [BucketName](#cfn-appflow-flow-s3sourceproperties-bucketname): String
  [BucketPrefix](#cfn-appflow-flow-s3sourceproperties-bucketprefix): String
```

## Properties<a name="aws-properties-appflow-flow-s3sourceproperties-properties"></a>

`BucketName`  <a name="cfn-appflow-flow-s3sourceproperties-bucketname"></a>
 The Amazon S3 bucket name where the source files are stored\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketPrefix`  <a name="cfn-appflow-flow-s3sourceproperties-bucketprefix"></a>
 The object key for the Amazon S3 bucket in which the source files are stored\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-s3sourceproperties--seealso"></a>
+ [S3SourceProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_S3SourceProperties.html) in the *Amazon AppFlow API Reference*\.

