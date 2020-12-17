# AWS::CloudFront::StreamingDistribution S3Origin<a name="aws-properties-cloudfront-streamingdistribution-s3origin"></a>

A complex type that contains information about the Amazon S3 bucket from which you want CloudFront to get your media files for distribution\.

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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginAccessIdentity`  <a name="cfn-cloudfront-streamingdistribution-s3origin-originaccessidentity"></a>
The CloudFront origin access identity to associate with the distribution\. Use an origin access identity to configure the distribution so that end users can only access objects in an Amazon S3 bucket through CloudFront\.  
If you want end users to be able to access objects using either the CloudFront URL or the Amazon S3 URL, specify an empty `OriginAccessIdentity` element\.  
To delete the origin access identity from an existing distribution, update the distribution configuration and include an empty `OriginAccessIdentity` element\.  
To replace the origin access identity, update the distribution configuration and specify the new origin access identity\.  
For more information, see [Using an Origin Access Identity to Restrict Access to Your Amazon S3 Content](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html) in the * Amazon CloudFront Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-cloudfront-streamingdistribution-s3origin--seealso"></a>
+  [S3Origin](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_S3Origin.html) in the *Amazon CloudFront API Reference* 

