# AWS::CloudFront::OriginRequestPolicy<a name="aws-resource-cloudfront-originrequestpolicy"></a>

An origin request policy\.

When it’s attached to a cache behavior, the origin request policy determines the values that CloudFront includes in requests that it sends to the origin\. Each request that CloudFront sends to the origin includes the following:
+ The request body and the URL path \(without the domain name\) from the viewer request\.
+ The headers that CloudFront automatically includes in every origin request, including `Host`, `User-Agent`, and `X-Amz-Cf-Id`\.
+ All HTTP headers, cookies, and URL query strings that are specified in the cache policy or the origin request policy\. These can include items from the viewer request and, in the case of headers, additional ones that are added by CloudFront\.

CloudFront sends a request when it can’t find an object in its cache that matches the request\. If you want to send values to the origin and also include them in the cache key, use `CachePolicy`\.

## Syntax<a name="aws-resource-cloudfront-originrequestpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudfront-originrequestpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFront::OriginRequestPolicy",
  "Properties" : {
      "[OriginRequestPolicyConfig](#cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig)" : OriginRequestPolicyConfig
    }
}
```

### YAML<a name="aws-resource-cloudfront-originrequestpolicy-syntax.yaml"></a>

```
Type: AWS::CloudFront::OriginRequestPolicy
Properties: 
  [OriginRequestPolicyConfig](#cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig): 
    OriginRequestPolicyConfig
```

## Properties<a name="aws-resource-cloudfront-originrequestpolicy-properties"></a>

`OriginRequestPolicyConfig`  <a name="cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig"></a>
The origin request policy configuration\.  
*Required*: Yes  
*Type*: [OriginRequestPolicyConfig](aws-properties-cloudfront-originrequestpolicy-originrequestpolicyconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudfront-originrequestpolicy-return-values"></a>

### Ref<a name="aws-resource-cloudfront-originrequestpolicy-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the origin request policy ID\. For example: `befd7079-9bbc-4ebf-8ade-498a3694176c`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudfront-originrequestpolicy-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudfront-originrequestpolicy-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The unique identifier for the origin request policy\. For example: `befd7079-9bbc-4ebf-8ade-498a3694176c`\.

`LastModifiedTime`  <a name="LastModifiedTime-fn::getatt"></a>
The date and time when the origin request policy was last modified\.