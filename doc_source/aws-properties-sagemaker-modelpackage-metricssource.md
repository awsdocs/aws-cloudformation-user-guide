# AWS::SageMaker::ModelPackage MetricsSource<a name="aws-properties-sagemaker-modelpackage-metricssource"></a>

Details about the metrics source\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-metricssource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-metricssource-syntax.json"></a>

```
{
  "[ContentDigest](#cfn-sagemaker-modelpackage-metricssource-contentdigest)" : String,
  "[ContentType](#cfn-sagemaker-modelpackage-metricssource-contenttype)" : String,
  "[S3Uri](#cfn-sagemaker-modelpackage-metricssource-s3uri)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-metricssource-syntax.yaml"></a>

```
  [ContentDigest](#cfn-sagemaker-modelpackage-metricssource-contentdigest): String
  [ContentType](#cfn-sagemaker-modelpackage-metricssource-contenttype): String
  [S3Uri](#cfn-sagemaker-modelpackage-metricssource-s3uri): String
```

## Properties<a name="aws-properties-sagemaker-modelpackage-metricssource-properties"></a>

`ContentDigest`  <a name="cfn-sagemaker-modelpackage-metricssource-contentdigest"></a>
The hash key used for the metrics source\.  
*Required*: No  
*Type*: String  
*Maximum*: `72`  
*Pattern*: `^[Ss][Hh][Aa]256:[0-9a-fA-F]{64}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ContentType`  <a name="cfn-sagemaker-modelpackage-metricssource-contenttype"></a>
The metric source content type\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3Uri`  <a name="cfn-sagemaker-modelpackage-metricssource-s3uri"></a>
The S3 URI for the metrics source\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(https|s3)://([^/]+)/?(.*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)