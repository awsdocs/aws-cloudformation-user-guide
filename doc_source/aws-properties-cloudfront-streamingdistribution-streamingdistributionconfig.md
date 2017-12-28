# Amazon CloudFront StreamingDistribution StreamingDistributionConfig<a name="aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig"></a>

<a name="aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig-description"></a>The `StreamingDistributionConfig` property type specifies the configuration of an RMTP streaming distribution for Amazon CloudFront\.

<a name="aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig-inheritance"></a> `StreamingDistributionConfig` is a property of the [AWS::CloudFront::StreamingDistribution](aws-resource-cloudfront-streamingdistribution.md) resource\. 

## Syntax<a name="aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-aliases)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-comment)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-enabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-logging)" : Logging,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-priceclass)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-s3origin)" : S3Origin,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-trustedsigners)" : TrustedSigners
}
```

### YAML<a name="aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-aliases): 
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-comment): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-enabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-logging): 
  Logging
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-priceclass): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-s3origin): 
  S3Origin
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-trustedsigners): 
  TrustedSigners
```

## Properties<a name="aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig-properties"></a>

For more information and valid property values, see [CreateStreamingDistribution](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CreateStreamingDistribution.html) in the *Amazon CloudFront API Reference*\.

`Aliases`  
Lists the CNAMEs \(alternate domain names\), if any, for this streaming distribution\.  
 *Required*: No  
 *Type*: StringList  
 *Update requires*: No interruption 

`Comment`  
Any comments you want to include about the streaming distribution\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`Enabled`  
Whether the streaming distribution is enabled to accept user requests for content\.  
 *Required*: Yes  
 *Type*: Boolean  
 *Update requires*: No interruption 

`Logging`  
Whether access logs are written for the streaming distribution\.  
 *Required*: No  
 *Type*: [CloudFront StreamingDistribution Logging](aws-properties-cloudfront-streamingdistribution-logging.md)  
 *Update requires*: No interruption 

`PriceClass`  
The price class for this streaming distribution\.  
Valid values include `PriceClass_100`, `PriceClass_200`, and `PriceClass_All`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`S3Origin`  
Information about the Amazon S3 bucket from which you want CloudFront to get your media files for distribution\.  
 *Required*: Yes  
 *Type*: [CloudFront StreamingDistribution S3Origin](aws-properties-cloudfront-streamingdistribution-s3origin.md)  
 *Update requires*: No interruption 

`TrustedSigners`  
Specifies any AWS accounts that you want to permit to create signed URLs for private content\. If you want the distribution to use signed URLs, include this element; if you want the distribution to use public URLs, remove this property\. For more information, see [Serving Private Content through CloudFront](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html) in the *Amazon CloudFront Developer Guide*\.  
 *Required*: Yes  
 *Type*: [CloudFront StreamingDistribution TrustedSigners](aws-properties-cloudfront-streamingdistribution-trustedsigners.md)  
 *Update requires*: No interruption 

## See Also<a name="aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig-seealso"></a>

+ [CreateStreamingDistribution](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CreateStreamingDistribution.html)