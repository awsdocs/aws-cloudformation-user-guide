# AWS::CloudFront::CachePolicy<a name="aws-resource-cloudfront-cachepolicy"></a>

A cache policy\.

When it’s attached to a cache behavior, the cache policy determines the following:
+ The values that CloudFront includes in the cache key\. These values can include HTTP headers, cookies, and URL query strings\. CloudFront uses the cache key to find an object in its cache that it can return to the viewer\.
+ The default, minimum, and maximum time to live \(TTL\) values that you want objects to stay in the CloudFront cache\.

The headers, cookies, and query strings that are included in the cache key are automatically included in requests that CloudFront sends to the origin\. CloudFront sends a request when it can’t find a valid object in its cache that matches the request’s cache key\. If you want to send values to the origin but *not* include them in the cache key, use `OriginRequestPolicy`\.

## Syntax<a name="aws-resource-cloudfront-cachepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudfront-cachepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFront::CachePolicy",
  "Properties" : {
      "[CachePolicyConfig](#cfn-cloudfront-cachepolicy-cachepolicyconfig)" : CachePolicyConfig
    }
}
```

### YAML<a name="aws-resource-cloudfront-cachepolicy-syntax.yaml"></a>

```
Type: AWS::CloudFront::CachePolicy
Properties: 
  [CachePolicyConfig](#cfn-cloudfront-cachepolicy-cachepolicyconfig): 
    CachePolicyConfig
```

## Properties<a name="aws-resource-cloudfront-cachepolicy-properties"></a>

`CachePolicyConfig`  <a name="cfn-cloudfront-cachepolicy-cachepolicyconfig"></a>
The cache policy configuration\.  
*Required*: Yes  
*Type*: [CachePolicyConfig](aws-properties-cloudfront-cachepolicy-cachepolicyconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudfront-cachepolicy-return-values"></a>

### Ref<a name="aws-resource-cloudfront-cachepolicy-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the cache policy ID\. For example: `2766f7b2-75c5-41c6-8f06-bf4303a2f2f5`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudfront-cachepolicy-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudfront-cachepolicy-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The unique identifier for the cache policy\. For example: `2766f7b2-75c5-41c6-8f06-bf4303a2f2f5`\.

`LastModifiedTime`  <a name="LastModifiedTime-fn::getatt"></a>
The date and time when the cache policy was last modified\.