# AWS::CloudFront::StreamingDistribution Logging<a name="aws-properties-cloudfront-streamingdistribution-logging"></a>

A complex type that controls whether access logs are written for the streaming distribution\. 

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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-cloudfront-streamingdistribution-logging-enabled"></a>
Specifies whether you want CloudFront to save access logs to an Amazon S3 bucket\. If you don't want to enable logging when you create a streaming distribution or if you want to disable logging for an existing streaming distribution, specify `false` for `Enabled`, and specify `empty Bucket` and `Prefix` elements\. If you specify `false` for `Enabled` but you specify values for `Bucket` and `Prefix`, the values are automatically deleted\.   
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-cloudfront-streamingdistribution-logging-prefix"></a>
An optional string that you want CloudFront to prefix to the access log filenames for this streaming distribution, for example, `myprefix/`\. If you want to enable logging, but you don't want to specify a prefix, you still must include an empty `Prefix` element in the `Logging` element\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-cloudfront-streamingdistribution-logging--seealso"></a>
+  [StreamingLoggingConfig](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_StreamingLoggingConfig.html) in the *Amazon CloudFront API Reference* 

