# AWS::CloudFront::CloudFrontOriginAccessIdentity<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity"></a>

The request to create a new origin access identity \(OAI\)\. An origin access identity is a special CloudFront user that you can associate with Amazon S3 origins, so that you can secure all or just some of your Amazon S3 content\. For more information, see [ Restricting Access to Amazon S3 Content by Using an Origin Access Identity](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html) in the *Amazon CloudFront Developer Guide*\. 

## Syntax<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFront::CloudFrontOriginAccessIdentity",
  "Properties" : {
      "[CloudFrontOriginAccessIdentityConfig](#cfn-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig)" : CloudFrontOriginAccessIdentityConfig
    }
}
```

### YAML<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-syntax.yaml"></a>

```
Type: AWS::CloudFront::CloudFrontOriginAccessIdentity
Properties: 
  [CloudFrontOriginAccessIdentityConfig](#cfn-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig): 
    CloudFrontOriginAccessIdentityConfig
```

## Properties<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-properties"></a>

`CloudFrontOriginAccessIdentityConfig`  <a name="cfn-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig"></a>
The current configuration information for the identity\.  
*Required*: Yes  
*Type*: [CloudFrontOriginAccessIdentityConfig](aws-properties-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-return-values"></a>

### Ref<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the origin access identity, such as `E15MNIMTCFKK4C`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-return-values-fn--getatt-fn--getatt"></a>

`S3CanonicalUserId`  <a name="S3CanonicalUserId-fn::getatt"></a>
The Amazon S3 canonical user ID for the origin access identity, used when giving the origin access identity read permission to an object in Amazon S3\. For example: `b970b42360b81c8ddbd79d2f5df0069ba9033c8a79655752abe380cd6d63ba8bcf23384d568fcf89fc49700b5e11a0fd`\.

## Examples<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity--examples"></a>



### Specify the comment for an origin access identity<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity--examples--Specify_the_comment_for_an_origin_access_identity"></a>



#### JSON<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity--examples--Specify_the_comment_for_an_origin_access_identity--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "cloudfrontoriginaccessidentity": {
            "Type": "AWS::CloudFront::CloudFrontOriginAccessIdentity",
            "Properties": {
                "CloudFrontOriginAccessIdentityConfig": {
                    "Comment": "string-value"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity--examples--Specify_the_comment_for_an_origin_access_identity--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  cloudfrontoriginaccessidentity:
    Type: AWS::CloudFront::CloudFrontOriginAccessIdentity
    Properties:
      CloudFrontOriginAccessIdentityConfig:
        Comment: string-value
```

## See also<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity--seealso"></a>
+  [OriginAccessIdentity](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_S3OriginConfig.html#cloudfront-Type-S3OriginConfig-OriginAccessIdentity) in the *Amazon CloudFront API Reference* 

