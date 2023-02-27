# AWS::SageMaker::ModelPackage DataSource<a name="aws-properties-sagemaker-modelpackage-datasource"></a>

Describes the location of the channel data\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-datasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-datasource-syntax.json"></a>

```
{
  "[S3DataSource](#cfn-sagemaker-modelpackage-datasource-s3datasource)" : S3DataSource
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-datasource-syntax.yaml"></a>

```
  [S3DataSource](#cfn-sagemaker-modelpackage-datasource-s3datasource): 
    S3DataSource
```

## Properties<a name="aws-properties-sagemaker-modelpackage-datasource-properties"></a>

`S3DataSource`  <a name="cfn-sagemaker-modelpackage-datasource-s3datasource"></a>
The S3 location of the data source that is associated with a channel\.  
*Required*: Yes  
*Type*: [S3DataSource](aws-properties-sagemaker-modelpackage-s3datasource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)