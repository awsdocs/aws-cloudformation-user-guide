# AWS::CloudFront::StreamingDistribution TrustedSigners<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners"></a>

Specifies the AWS accounts, if any, that you want to allow to create signed URLs for private content\.

If you want to require signed URLs in requests for objects in the target origin, specify `true` for `Enabled`, and specify a list of AWS account IDs\. For more information, see [Serving Private Content through CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html) in the * Amazon CloudFront Developer Guide*\.

If you don't want to require signed URLs in requests for objects, specify `false` for `Enabled` and omit the list of AWS account IDs\.

## Syntax<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners-syntax.json"></a>

```
{
  "[AwsAccountNumbers](#cfn-cloudfront-streamingdistribution-trustedsigners-awsaccountnumbers)" : [ String, ... ],
  "[Enabled](#cfn-cloudfront-streamingdistribution-trustedsigners-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners-syntax.yaml"></a>

```
  [AwsAccountNumbers](#cfn-cloudfront-streamingdistribution-trustedsigners-awsaccountnumbers): 
    - String
  [Enabled](#cfn-cloudfront-streamingdistribution-trustedsigners-enabled): Boolean
```

## Properties<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners-properties"></a>

`AwsAccountNumbers`  <a name="cfn-cloudfront-streamingdistribution-trustedsigners-awsaccountnumbers"></a>
An AWS account that is included in the `TrustedSigners` complex type for this distribution\. Valid values include:  
+  `self`, which is the AWS account used to create the distribution\.
+ An AWS account number\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-cloudfront-streamingdistribution-trustedsigners-enabled"></a>
Specifies whether you want to require viewers to use signed URLs to access the files specified by `PathPattern` and `TargetOriginId`\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners--seealso"></a>
+  [TrustedSigners](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_TrustedSigners.html) in the *Amazon CloudFront API Reference* 