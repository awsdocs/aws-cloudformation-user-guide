# AWS::CloudFront::Distribution Logging<a name="aws-properties-cloudfront-distribution-logging"></a>

A complex type that controls whether access logs are written for the distribution\.

## Syntax<a name="aws-properties-cloudfront-distribution-logging-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-cloudfront-distribution-logging-properties"></a>

`Bucket`  <a name="cfn-cloudfront-distribution-logging-bucket"></a>
The Amazon S3 bucket to store the access logs in, for example, `myawslogbucket.s3.amazonaws.com`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeCookies`  <a name="cfn-cloudfront-distribution-logging-includecookies"></a>
Specifies whether you want CloudFront to include cookies in access logs, specify `true` for `IncludeCookies`\. If you choose to include cookies in logs, CloudFront logs all cookies regardless of how you configure the cache behaviors for this distribution\. If you don't want to include cookies when you create a distribution or if you want to disable include cookies for an existing distribution, specify `false` for `IncludeCookies`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-cloudfront-distribution-logging-prefix"></a>
An optional string that you want CloudFront to prefix to the access log `filenames` for this distribution, for example, `myprefix/`\. If you want to enable logging, but you don't want to specify a prefix, you still must include an empty `Prefix` element in the `Logging` element\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-cloudfront-distribution-logging--seealso"></a>
+  [LoggingConfig](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_LoggingConfig.html) in the *Amazon CloudFront API Reference* 

