# AWS::CloudFront::ResponseHeadersPolicy<a name="aws-resource-cloudfront-responseheaderspolicy"></a>

A response headers policy\.

A response headers policy contains information about a set of HTTP response headers\.

After you create a response headers policy, you can use its ID to attach it to one or more cache behaviors in a CloudFront distribution\. When it's attached to a cache behavior, the response headers policy affects the HTTP headers that CloudFront includes in HTTP responses to requests that match the cache behavior\. CloudFront adds or removes response headers according to the configuration of the response headers policy\.

For more information, see [Adding or removing HTTP headers in CloudFront responses](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/modifying-response-headers.html) in the *Amazon CloudFront Developer Guide*\.

## Syntax<a name="aws-resource-cloudfront-responseheaderspolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudfront-responseheaderspolicy-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFront::ResponseHeadersPolicy",
  "Properties" : {
      "[ResponseHeadersPolicyConfig](#cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig)" : ResponseHeadersPolicyConfig
    }
}
```

### YAML<a name="aws-resource-cloudfront-responseheaderspolicy-syntax.yaml"></a>

```
Type: AWS::CloudFront::ResponseHeadersPolicy
Properties: 
  [ResponseHeadersPolicyConfig](#cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig): 
    ResponseHeadersPolicyConfig
```

## Properties<a name="aws-resource-cloudfront-responseheaderspolicy-properties"></a>

`ResponseHeadersPolicyConfig`  <a name="cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig"></a>
A response headers policy configuration\.  
*Required*: Yes  
*Type*: [ResponseHeadersPolicyConfig](aws-properties-cloudfront-responseheaderspolicy-responseheaderspolicyconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudfront-responseheaderspolicy-return-values"></a>

### Ref<a name="aws-resource-cloudfront-responseheaderspolicy-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the response headers policy ID\. For example: `57f99797-3b20-4e1b-a728-27972a74082a`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudfront-responseheaderspolicy-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudfront-responseheaderspolicy-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The unique identifier for the response headers policy\. For example: `57f99797-3b20-4e1b-a728-27972a74082a`\.

`LastModifiedTime`  <a name="LastModifiedTime-fn::getatt"></a>
The date and time when the response headers policy was last modified\.