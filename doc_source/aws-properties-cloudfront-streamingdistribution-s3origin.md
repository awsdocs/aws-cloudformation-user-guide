# Amazon CloudFront StreamingDistribution S3Origin<a name="aws-properties-cloudfront-streamingdistribution-s3origin"></a>

<a name="aws-properties-cloudfront-streamingdistribution-s3origin-description"></a>The `S3Origin` property type specifies information about the Amazon S3 bucket from which you want Amazon CloudFront to get your media files for distribution\. For more information, see [S3Origin](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_S3Origin.html) in the *Amazon CloudFront API Reference*\.

<a name="aws-properties-cloudfront-streamingdistribution-s3origin-inheritance"></a> `S3Origin` is a property of the [CloudFront StreamingDistribution StreamingDistributionConfig](aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig.md) property type\. 

## Syntax<a name="aws-properties-cloudfront-streamingdistribution-s3origin-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-streamingdistribution-s3origin-syntax.json"></a>

```
{
  "[DomainName](#cfn-cloudfront-streamingdistribution-s3origin-domainname)" : String,
  "[OriginAccessIdentity](#cfn-cloudfront-streamingdistribution-s3origin-originaccessidentity)" : String
}
```

### YAML<a name="aws-properties-cloudfront-streamingdistribution-s3origin-syntax.yaml"></a>

```
[DomainName](#cfn-cloudfront-streamingdistribution-s3origin-domainname): String
[OriginAccessIdentity](#cfn-cloudfront-streamingdistribution-s3origin-originaccessidentity): String
```

## Properties<a name="aws-properties-cloudfront-streamingdistribution-s3origin-properties"></a>

`DomainName`  <a name="cfn-cloudfront-streamingdistribution-s3origin-domainname"></a>
The DNS name of the Amazon S3 origin\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`OriginAccessIdentity`  <a name="cfn-cloudfront-streamingdistribution-s3origin-originaccessidentity"></a>
The CloudFront origin access identity to associate with the RTMP distribution\. Use an origin access identity to configure the distribution so that end users can only access objects in an Amazon S3 bucket through CloudFront\. For more information, see the `OriginAccessIdentity` property for [S3Origin](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_S3Origin.html) in *Amazon CloudFront API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-cloudfront-streamingdistribution-s3origin-seealso"></a>
+ [S3Origin](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_S3Origin.html) in the *Amazon CloudFront API Reference*