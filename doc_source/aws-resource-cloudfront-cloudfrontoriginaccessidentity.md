# AWS::CloudFront::CloudFrontOriginAccessIdentity<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity"></a>

The `AWS::CloudFront::CloudFrontOriginAccessIdentity` resource specifies the CloudFront origin access identity to associate with the origin of a CloudFront distribution\. For more information, see [OriginAccessIdentity](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_S3OriginConfig.html#cloudfront-Type-S3OriginConfig-OriginAccessIdentity) in the *Amazon CloudFront API Reference*\. 

**Topics**
+ [Syntax](#aws-resource-cloudfront-cloudfrontoriginaccessidentity-syntax)
+ [Properties](#aws-resource-cloudfront-cloudfrontoriginaccessidentity-properties)
+ [Return Values](#aws-resource-cloudfront-cloudfrontoriginaccessidentity-returnvalues)
+ [Example](#aws-resource-cloudfront-cloudfrontoriginaccessidentity-examples)
+ [See Also](#aws-resource-cloudfront-cloudfrontoriginaccessidentity-seealso)

## Syntax<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFront::CloudFrontOriginAccessIdentity",
  "Properties" : {
    "[CloudFrontOriginAccessIdentityConfig](#cfn-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig)" : [*CloudFrontOriginAccessIdentityConfig*](aws-properties-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig.md)
  }
}
```

### YAML<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-syntax.yaml"></a>

```
Type: "AWS::CloudFront::CloudFrontOriginAccessIdentity"
Properties:
  [CloudFrontOriginAccessIdentityConfig](#cfn-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig): CloudFrontOriginAccessIdentityConfig
```

## Properties<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-properties"></a>

`CloudFrontOriginAccessIdentityConfig`  <a name="cfn-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig"></a>
The configuration of the CloudFront origin access identity\.  
 *Required*: Yes  
 *Type*: [CloudFrontOriginAccessIdentityConfig](aws-properties-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-returnvalues"></a>

### Ref<a name="w3ab2c21c10d219c11b3"></a>

When you pass the logical ID of an `AWS::CloudFront::CloudFrontOriginAccessIdentity` resource to the intrinsic `Ref` function, the function returns the origin access identity, such as `E15MNIMTCFKK4C`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="w3ab2c21c10d219c11b5"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`S3CanonicalUserId`  
The Amazon S3 canonical user ID for the origin access identity, used when giving the origin access identity read permission to an object in Amazon S3\. For example: `b970b42360b81c8ddbd79d2f5df0069ba9033c8a79655752abe380cd6d63ba8bcf23384d568fcf89fc49700b5e11a0fd`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Example<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-examples"></a>

### <a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-example1"></a>

The following example specifies the comment for an origin access identity\.

#### JSON<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-example1.json"></a>

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

#### YAML<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  cloudfrontoriginaccessidentity:
    Type: 'AWS::CloudFront::CloudFrontOriginAccessIdentity'
    Properties:
      CloudFrontOriginAccessIdentityConfig:
        Comment: string-value
```

## See Also<a name="aws-resource-cloudfront-cloudfrontoriginaccessidentity-seealso"></a>
+ [OriginAccessIdentity](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_S3OriginConfig.html#cloudfront-Type-S3OriginConfig-OriginAccessIdentity) in the *Amazon CloudFront API Reference*