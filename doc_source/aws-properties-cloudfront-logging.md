# CloudFront Logging<a name="aws-properties-cloudfront-logging"></a>

`Logging` is a property of the DistributionConfig property that enables Amazon CloudFront to deliver access logs for each distribution to an Amazon Simple Storage Service \(S3\) bucket\.

## Syntax<a name="w3ab2c21c14d195b5"></a>

### JSON<a name="aws-properties-cloudfront-logging-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-logging-bucket)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-logging-includecookies)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-logging-prefix)" : String
}
```

### YAML<a name="aws-properties-cloudfront-logging-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-logging-bucket): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-logging-includecookies): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-logging-prefix): String
```

## Properties<a name="w3ab2c21c14d195b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [LoggingConfig](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_LoggingConfig.html) data type in the *Amazon CloudFront API Reference*\.

`Bucket`  
The Amazon S3 bucket address where access logs are stored, for example, `mybucket.s3.amazonaws.com`\.  
*Required: *Yes  
*Type*: String

`IncludeCookies`  
Indicates whether CloudFront includes cookies in access logs\.  
*Required: *No  
*Type*: Boolean

`Prefix`  
A prefix for the access log file names for this distribution\.  
*Required: *No  
*Type*: String