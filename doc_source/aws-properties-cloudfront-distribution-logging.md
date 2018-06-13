# CloudFront Distribution Logging<a name="aws-properties-cloudfront-distribution-logging"></a>

`Logging` is a property of the [DistributionConfig](aws-properties-cloudfront-distribution-distributionconfig.md) property that enables Amazon CloudFront to deliver access logs for each distribution to an Amazon Simple Storage Service \(S3\) bucket\.

## Syntax<a name="w3ab2c21c14d285b5"></a>

### JSON<a name="aws-properties-cloudfront-distribution-logging-syntax.json"></a>

```
{
  "[Bucket](#cfn-cloudfront-distribution-logging-bucket)" : String,
  "[IncludeCookies](#cfn-cloudfront-distribution-logging-includecookies)" : Boolean,
  "[Prefix](#cfn-cloudfront-distribution-logging-prefix)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distribution-logging-syntax.yaml"></a>

```
[Bucket](#cfn-cloudfront-distribution-logging-bucket): String
[IncludeCookies](#cfn-cloudfront-distribution-logging-includecookies): Boolean
[Prefix](#cfn-cloudfront-distribution-logging-prefix): String
```

## Properties<a name="w3ab2c21c14d285b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [LoggingConfig](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_LoggingConfig.html) data type in the *Amazon CloudFront API Reference*\.

`Bucket`  <a name="cfn-cloudfront-distribution-logging-bucket"></a>
The Amazon S3 bucket address where access logs are stored, for example, `mybucket.s3.amazonaws.com`\.  
*Required*: Yes  
*Type*: String

`IncludeCookies`  <a name="cfn-cloudfront-distribution-logging-includecookies"></a>
Indicates whether CloudFront includes cookies in access logs\.  
*Required*: No  
*Type*: Boolean

`Prefix`  <a name="cfn-cloudfront-distribution-logging-prefix"></a>
A prefix for the access log file names for this distribution\.  
*Required*: No  
*Type*: String