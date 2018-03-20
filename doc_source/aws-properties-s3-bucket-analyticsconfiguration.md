# Amazon S3 Bucket AnalyticsConfiguration<a name="aws-properties-s3-bucket-analyticsconfiguration"></a>

<a name="aws-properties-s3-bucket-analyticsconfiguration-description"></a>The `AnalyticsConfiguration` property type specifies the configuration and any analyses for the analytics filter of an Amazon S3 bucket\.

For more information, see [GET Bucket analytics](http://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketGETAnalyticsConfig.html) in the *Amazon Simple Storage Service API Reference*

<a name="aws-properties-s3-bucket-analyticsconfiguration-inheritance"></a> `AnalyticsConfigurations` is a property of the [AWS::S3::Bucket](aws-properties-s3-bucket.md) resource type\. 

## Syntax<a name="aws-properties-s3-bucket-analyticsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-analyticsconfiguration-syntax.json"></a>

```
{
  "[Id](#cfn-s3-bucket-analyticsconfiguration-id)" : String,
  "[Prefix](#cfn-s3-bucket-analyticsconfiguration-prefix)" : String,
  "[StorageClassAnalysis](#cfn-s3-bucket-analyticsconfiguration-storageclassanalysis)" : [*StorageClassAnalysis*](aws-properties-s3-bucket-storageclassanalysis.md),
  "[TagFilters](#cfn-s3-bucket-analyticsconfiguration-tagfilters)" : [ [*TagFilter*](aws-properties-s3-bucket-tagfilter.md), ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-analyticsconfiguration-syntax.yaml"></a>

```
[Id](#cfn-s3-bucket-analyticsconfiguration-id): String
[Prefix](#cfn-s3-bucket-analyticsconfiguration-prefix): String
[StorageClassAnalysis](#cfn-s3-bucket-analyticsconfiguration-storageclassanalysis): StorageClassAnalysis
[TagFilters](#cfn-s3-bucket-analyticsconfiguration-tagfilters): 
  - [*TagFilter*](aws-properties-s3-bucket-tagfilter.md)
```

## Properties<a name="aws-properties-s3-bucket-analyticsconfiguration-properties"></a>

`Id`  <a name="cfn-s3-bucket-analyticsconfiguration-id"></a>
The ID that identifies the analytics configuration\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Prefix`  <a name="cfn-s3-bucket-analyticsconfiguration-prefix"></a>
The prefix that an object must have to be included in the analytics results\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`StorageClassAnalysis`  <a name="cfn-s3-bucket-analyticsconfiguration-storageclassanalysis"></a>
Contains data related to access patterns to be collected and made available to analyze the tradeoffs between different storage classes\.  
 *Required*: Yes  
 *Type*: [Amazon S3 Bucket StorageClassAnalysis](aws-properties-s3-bucket-storageclassanalysis.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TagFilters`  <a name="cfn-s3-bucket-analyticsconfiguration-tagfilters"></a>
The tags to use when evaluating an analytics filter\.  
The analytics only includes objects that meet the filter's criteria\. If no filter is speciified, all of the contents of the bucket are included in the analysis\.  
 *Required*: No  
 *Type*: List of [Amazon S3 Bucket TagFilter](aws-properties-s3-bucket-tagfilter.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 