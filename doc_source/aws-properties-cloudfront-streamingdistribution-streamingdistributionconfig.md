# AWS::CloudFront::StreamingDistribution StreamingDistributionConfig<a name="aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig"></a>

The RTMP distribution's configuration information\.

## Syntax<a name="aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig-syntax.json"></a>

```
{
  "[Aliases](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-aliases)" : [ String, ... ],
  "[Comment](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-comment)" : String,
  "[Enabled](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-enabled)" : Boolean,
  "[Logging](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-logging)" : Logging,
  "[PriceClass](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-priceclass)" : String,
  "[S3Origin](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-s3origin)" : S3Origin,
  "[TrustedSigners](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-trustedsigners)" : TrustedSigners
}
```

### YAML<a name="aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig-syntax.yaml"></a>

```
  [Aliases](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-aliases): 
    - String
  [Comment](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-comment): String
  [Enabled](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-enabled): Boolean
  [Logging](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-logging): 
    Logging
  [PriceClass](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-priceclass): String
  [S3Origin](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-s3origin): 
    S3Origin
  [TrustedSigners](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig-trustedsigners): 
    TrustedSigners
```

## Properties<a name="aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig-properties"></a>

`Aliases`  <a name="cfn-cloudfront-streamingdistribution-streamingdistributionconfig-aliases"></a>
A complex type that contains information about CNAMEs \(alternate domain names\), if any, for this streaming distribution\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Comment`  <a name="cfn-cloudfront-streamingdistribution-streamingdistributionconfig-comment"></a>
Any comments you want to include about the streaming distribution\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-cloudfront-streamingdistribution-streamingdistributionconfig-enabled"></a>
Whether the streaming distribution is enabled to accept user requests for content\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Logging`  <a name="cfn-cloudfront-streamingdistribution-streamingdistributionconfig-logging"></a>
A complex type that controls whether access logs are written for the streaming distribution\.   
*Required*: No  
*Type*: [Logging](aws-properties-cloudfront-streamingdistribution-logging.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PriceClass`  <a name="cfn-cloudfront-streamingdistribution-streamingdistributionconfig-priceclass"></a>
A complex type that contains information about price class for this streaming distribution\.   
*Required*: No  
*Type*: String  
*Allowed values*: `PriceClass_100 | PriceClass_200 | PriceClass_All`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Origin`  <a name="cfn-cloudfront-streamingdistribution-streamingdistributionconfig-s3origin"></a>
A complex type that contains information about the Amazon S3 bucket from which you want CloudFront to get your media files for distribution\.   
*Required*: Yes  
*Type*: [S3Origin](aws-properties-cloudfront-streamingdistribution-s3origin.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrustedSigners`  <a name="cfn-cloudfront-streamingdistribution-streamingdistributionconfig-trustedsigners"></a>
A complex type that specifies any AWS accounts that you want to permit to create signed URLs for private content\. If you want the distribution to use signed URLs, include this element; if you want the distribution to use public URLs, remove this element\. For more information, see [Serving Private Content through CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html) in the *Amazon CloudFront Developer Guide*\.   
*Required*: Yes  
*Type*: [TrustedSigners](aws-properties-cloudfront-streamingdistribution-trustedsigners.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig--seealso"></a>
+  [StreamingDistributionConfig](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_StreamingDistributionConfig.html) in the *Amazon CloudFront API Reference* 

