# AWS::CloudFront::Distribution S3OriginConfig<a name="aws-properties-cloudfront-distribution-s3originconfig"></a>

A complex type that contains information about the Amazon S3 origin\. If the origin is a custom origin or an S3 bucket that is configured as a website endpoint, use the `CustomOriginConfig` element instead\.

## Syntax<a name="aws-properties-cloudfront-distribution-s3originconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-distribution-s3originconfig-syntax.json"></a>

```
{
  "[OriginAccessIdentity](#cfn-cloudfront-distribution-s3originconfig-originaccessidentity)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distribution-s3originconfig-syntax.yaml"></a>

```
  [OriginAccessIdentity](#cfn-cloudfront-distribution-s3originconfig-originaccessidentity): String
```

## Properties<a name="aws-properties-cloudfront-distribution-s3originconfig-properties"></a>

`OriginAccessIdentity`  <a name="cfn-cloudfront-distribution-s3originconfig-originaccessidentity"></a>
The CloudFront origin access identity to associate with the origin\. Use an origin access identity to configure the origin so that viewers can *only* access objects in an Amazon S3 bucket through CloudFront\. The format of the value is:  
origin\-access\-identity/cloudfront/*ID\-of\-origin\-access\-identity*   
where ` ID-of-origin-access-identity ` is the value that CloudFront returned in the `ID` element when you created the origin access identity\.  
If you want viewers to be able to access objects using either the CloudFront URL or the Amazon S3 URL, specify an empty `OriginAccessIdentity` element\.  
To delete the origin access identity from an existing distribution, update the distribution configuration and include an empty `OriginAccessIdentity` element\.  
To replace the origin access identity, update the distribution configuration and specify the new origin access identity\.  
For more information about the origin access identity, see [Serving Private Content through CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-cloudfront-distribution-s3originconfig--seealso"></a>
+  [S3OriginConfig](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_S3OriginConfig.html) in the *Amazon CloudFront API Reference* 

