# Amazon CloudFront CloudFrontOriginAccessIdentity CloudFrontOriginAccessIdentityConfig<a name="aws-properties-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig"></a>

<a name="aws-properties-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig-description"></a>The `CloudFrontOriginAccessIdentityConfig` property type configures the CloudFront origin access identity to associate with the origin of a CloudFront distribution\.

<a name="aws-properties-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig-inheritance"></a> `CloudFrontOriginAccessIdentityConfig` is a property of the [AWS::CloudFront::CloudFrontOriginAccessIdentity](aws-resource-cloudfront-cloudfrontoriginaccessidentity.md) resource\. 

## Syntax<a name="aws-properties-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig-syntax.json"></a>

```
{
  "[Comment](#cfn-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig-comment)" : String
}
```

### YAML<a name="aws-properties-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig-syntax.yaml"></a>

```
[Comment](#cfn-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig-comment): String
```

## Properties<a name="aws-properties-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig-properties"></a>

`Comment`  <a name="cfn-cloudfront-cloudfrontoriginaccessidentity-cloudfrontoriginaccessidentityconfig-comment"></a>
A comment to associate with this CloudFront origin access identity\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 