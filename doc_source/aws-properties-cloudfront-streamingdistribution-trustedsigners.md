# Amazon CloudFront StreamingDistribution TrustedSigners<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners"></a>

<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners-description"></a>The `TrustedSigners` property type specifies the AWS accounts, if any, that you want to allow to create signed URLs for private content for an Amazon CloudFront distribution\. For more information, see [TrustedSigners](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_TrustedSigners.html) in the *Amazon CloudFront API Reference*\.

<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners-inheritance"></a> `TrustedSigners` is a property of the [CloudFront StreamingDistribution StreamingDistributionConfig](aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig.md) property type\. 

## Syntax<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners-syntax.json"></a>

```
{
  "[AwsAccountNumbers](#cfn-cloudfront-streamingdistribution-trustedsigners-awsaccountnumbers)" : [ String, ... ]
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
The trusted signers for this cache behavior\.  
 *Required*: No  
 *Type*: StringList  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Enabled`  <a name="cfn-cloudfront-streamingdistribution-trustedsigners-enabled"></a>
Specifies whether you want to require viewers to use signed URLs to access the files specified by `PathPattern` and `TargetOriginId`\.  
 *Required*: Yes  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners-seealso"></a>
+ [TrustedSigners](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_TrustedSigners.html) in the *Amazon CloudFront API Reference*