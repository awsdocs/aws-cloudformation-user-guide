# AWS::S3ObjectLambda::AccessPoint ObjectLambdaConfiguration<a name="aws-properties-s3objectlambda-accesspoint-objectlambdaconfiguration"></a>

A configuration used when creating an Object Lambda Access Point\.

## Syntax<a name="aws-properties-s3objectlambda-accesspoint-objectlambdaconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3objectlambda-accesspoint-objectlambdaconfiguration-syntax.json"></a>

```
{
  "[AllowedFeatures](#cfn-s3objectlambda-accesspoint-objectlambdaconfiguration-allowedfeatures)" : [ String, ... ],
  "[CloudWatchMetricsEnabled](#cfn-s3objectlambda-accesspoint-objectlambdaconfiguration-cloudwatchmetricsenabled)" : Boolean,
  "[SupportingAccessPoint](#cfn-s3objectlambda-accesspoint-objectlambdaconfiguration-supportingaccesspoint)" : String,
  "[TransformationConfigurations](#cfn-s3objectlambda-accesspoint-objectlambdaconfiguration-transformationconfigurations)" : [ TransformationConfiguration, ... ]
}
```

### YAML<a name="aws-properties-s3objectlambda-accesspoint-objectlambdaconfiguration-syntax.yaml"></a>

```
  [AllowedFeatures](#cfn-s3objectlambda-accesspoint-objectlambdaconfiguration-allowedfeatures): 
    - String
  [CloudWatchMetricsEnabled](#cfn-s3objectlambda-accesspoint-objectlambdaconfiguration-cloudwatchmetricsenabled): Boolean
  [SupportingAccessPoint](#cfn-s3objectlambda-accesspoint-objectlambdaconfiguration-supportingaccesspoint): String
  [TransformationConfigurations](#cfn-s3objectlambda-accesspoint-objectlambdaconfiguration-transformationconfigurations): 
    - TransformationConfiguration
```

## Properties<a name="aws-properties-s3objectlambda-accesspoint-objectlambdaconfiguration-properties"></a>

`AllowedFeatures`  <a name="cfn-s3objectlambda-accesspoint-objectlambdaconfiguration-allowedfeatures"></a>
A container for allowed features\. Valid inputs are `GetObject-Range`, `GetObject-PartNumber`, `HeadObject-Range`, and `HeadObject-PartNumber`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloudWatchMetricsEnabled`  <a name="cfn-s3objectlambda-accesspoint-objectlambdaconfiguration-cloudwatchmetricsenabled"></a>
A container for whether the CloudWatch metrics configuration is enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupportingAccessPoint`  <a name="cfn-s3objectlambda-accesspoint-objectlambdaconfiguration-supportingaccesspoint"></a>
Standard access point associated with the Object Lambda Access Point\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransformationConfigurations`  <a name="cfn-s3objectlambda-accesspoint-objectlambdaconfiguration-transformationconfigurations"></a>
A container for transformation configurations for an Object Lambda Access Point\.  
*Required*: Yes  
*Type*: List of [TransformationConfiguration](aws-properties-s3objectlambda-accesspoint-transformationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)