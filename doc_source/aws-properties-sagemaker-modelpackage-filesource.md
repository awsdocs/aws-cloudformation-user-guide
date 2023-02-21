# AWS::SageMaker::ModelPackage FileSource<a name="aws-properties-sagemaker-modelpackage-filesource"></a>

Contains details regarding the file source\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-filesource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-filesource-syntax.json"></a>

```
{
  "[ContentDigest](#cfn-sagemaker-modelpackage-filesource-contentdigest)" : String,
  "[ContentType](#cfn-sagemaker-modelpackage-filesource-contenttype)" : String,
  "[S3Uri](#cfn-sagemaker-modelpackage-filesource-s3uri)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-filesource-syntax.yaml"></a>

```
  [ContentDigest](#cfn-sagemaker-modelpackage-filesource-contentdigest): String
  [ContentType](#cfn-sagemaker-modelpackage-filesource-contenttype): String
  [S3Uri](#cfn-sagemaker-modelpackage-filesource-s3uri): String
```

## Properties<a name="aws-properties-sagemaker-modelpackage-filesource-properties"></a>

`ContentDigest`  <a name="cfn-sagemaker-modelpackage-filesource-contentdigest"></a>
The digest of the file source\.  
*Required*: No  
*Type*: String  
*Maximum*: `72`  
*Pattern*: `^[Ss][Hh][Aa]256:[0-9a-fA-F]{64}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ContentType`  <a name="cfn-sagemaker-modelpackage-filesource-contenttype"></a>
The type of content stored in the file source\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3Uri`  <a name="cfn-sagemaker-modelpackage-filesource-s3uri"></a>
The Amazon S3 URI for the file source\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(https|s3)://([^/]+)/?(.*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)