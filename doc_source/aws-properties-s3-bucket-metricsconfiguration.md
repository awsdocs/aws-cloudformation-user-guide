# AWS::S3::Bucket MetricsConfiguration<a name="aws-properties-s3-bucket-metricsconfiguration"></a>

Specifies a metrics configuration for the CloudWatch request metrics \(specified by the metrics configuration ID\) from an Amazon S3 bucket\. If you're updating an existing metrics configuration, note that this is a full replacement of the existing metrics configuration\. If you don't include the elements you want to keep, they are erased\. For examples, see [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)\. For more information, see [ PUT Bucket metrics](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTMetricConfiguration.html) in the *Amazon Simple Storage Service API Reference*\.

## Syntax<a name="aws-properties-s3-bucket-metricsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-metricsconfiguration-syntax.json"></a>

```
{
  "[Id](#cfn-s3-bucket-metricsconfiguration-id)" : String,
  "[Prefix](#cfn-s3-bucket-metricsconfiguration-prefix)" : String,
  "[TagFilters](#cfn-s3-bucket-metricsconfiguration-tagfilters)" : [ TagFilter, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-metricsconfiguration-syntax.yaml"></a>

```
  [Id](#cfn-s3-bucket-metricsconfiguration-id): String
  [Prefix](#cfn-s3-bucket-metricsconfiguration-prefix): String
  [TagFilters](#cfn-s3-bucket-metricsconfiguration-tagfilters): 
    - TagFilter
```

## Properties<a name="aws-properties-s3-bucket-metricsconfiguration-properties"></a>

`Id`  <a name="cfn-s3-bucket-metricsconfiguration-id"></a>
The ID used to identify the metrics configuration\. This can be any value you choose that helps you identify your metrics configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-s3-bucket-metricsconfiguration-prefix"></a>
The prefix that an object must have to be included in the metrics results\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagFilters`  <a name="cfn-s3-bucket-metricsconfiguration-tagfilters"></a>
Specifies a list of tag filters to use as a metrics configuration filter\. The metrics configuration includes only objects that meet the filter's criteria\.  
*Required*: No  
*Type*: List of [TagFilter](aws-properties-s3-bucket-tagfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-metricsconfiguration--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

