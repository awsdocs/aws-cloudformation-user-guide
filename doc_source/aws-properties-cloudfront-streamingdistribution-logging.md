# Amazon CloudFront StreamingDistribution Logging<a name="aws-properties-cloudfront-streamingdistribution-logging"></a>

<a name="aws-properties-cloudfront-streamingdistribution-logging-description"></a>The `Logging` property type to control whether access logs are written for a Amazon CloudFront streaming distribution\.

<a name="aws-properties-cloudfront-streamingdistribution-logging-inheritance"></a> `Logging` is a property of the [CloudFront StreamingDistribution StreamingDistributionConfig](aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig.md) property type\. 

## Syntax<a name="aws-properties-cloudfront-streamingdistribution-logging-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-streamingdistribution-logging-syntax.json"></a>

```
{
  "[Bucket](#cfn-cloudfront-streamingdistribution-logging-bucket)" : String,
  "[Enabled](#cfn-cloudfront-streamingdistribution-logging-enabled)" : Boolean,
  "[Prefix](#cfn-cloudfront-streamingdistribution-logging-prefix)" : String
}
```

### YAML<a name="aws-properties-cloudfront-streamingdistribution-logging-syntax.yaml"></a>

```
[Bucket](#cfn-cloudfront-streamingdistribution-logging-bucket): String
[Enabled](#cfn-cloudfront-streamingdistribution-logging-enabled): Boolean
[Prefix](#cfn-cloudfront-streamingdistribution-logging-prefix): String
```

## Properties<a name="aws-properties-cloudfront-streamingdistribution-logging-properties"></a>

`Bucket`  <a name="cfn-cloudfront-streamingdistribution-logging-bucket"></a>
The Amazon S3 bucket to store the access logs in, for example, `myawslogbucket.s3.amazonaws.com`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Enabled`  <a name="cfn-cloudfront-streamingdistribution-logging-enabled"></a>
Specifies whether you want CloudFront to save access logs to an Amazon S3 bucket\. If you don't want to enable logging when you create a streaming distribution or if you want to disable logging for an existing streaming distribution, specify `false` for `Enabled`, and specify `empty Bucket` and `Prefix` elements\. If you specify `false` for `Enabled` but you specify values for `Bucket` and `Prefix`, the values are automatically deleted\.  
 *Required*: Yes  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Prefix`  <a name="cfn-cloudfront-streamingdistribution-logging-prefix"></a>
An optional string that you want CloudFront to prefix to the access log filenames for this streaming distribution, for example, `myprefix/`\. If you want to enable logging, but you don't want to specify a prefix, you still must include an empty `Prefix` property in the `Logging` property\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-cloudfront-streamingdistribution-logging-seealso"></a>
+ [StreamingLoggingConfig](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_StreamingLoggingConfig.html) in the *Amazon CloudFront API Reference*