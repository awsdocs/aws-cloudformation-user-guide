# AWS::CloudFront::CachePolicy QueryStringsConfig<a name="aws-properties-cloudfront-cachepolicy-querystringsconfig"></a>

An object that determines whether any URL query strings in viewer requests \(and if so, which query strings\) are included in the cache key and automatically included in requests that CloudFront sends to the origin\.

## Syntax<a name="aws-properties-cloudfront-cachepolicy-querystringsconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-cachepolicy-querystringsconfig-syntax.json"></a>

```
{
  "[QueryStringBehavior](#cfn-cloudfront-cachepolicy-querystringsconfig-querystringbehavior)" : String,
  "[QueryStrings](#cfn-cloudfront-cachepolicy-querystringsconfig-querystrings)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudfront-cachepolicy-querystringsconfig-syntax.yaml"></a>

```
  [QueryStringBehavior](#cfn-cloudfront-cachepolicy-querystringsconfig-querystringbehavior): 
    String
  [QueryStrings](#cfn-cloudfront-cachepolicy-querystringsconfig-querystrings): 
    - String
```

## Properties<a name="aws-properties-cloudfront-cachepolicy-querystringsconfig-properties"></a>

`QueryStringBehavior`  <a name="cfn-cloudfront-cachepolicy-querystringsconfig-querystringbehavior"></a>
Determines whether any URL query strings in viewer requests are included in the cache key and automatically included in requests that CloudFront sends to the origin\. Valid values are:  
+  `none` – Query strings in viewer requests are not included in the cache key and are not automatically included in requests that CloudFront sends to the origin\. Even when this field is set to `none`, any query strings that are listed in an `OriginRequestPolicy` *are* included in origin requests\.
+  `whitelist` – The query strings in viewer requests that are listed in the `QueryStringNames` type are included in the cache key and automatically included in requests that CloudFront sends to the origin\.
+  `allExcept` – All query strings in viewer requests that are * **not** * listed in the `QueryStringNames` type are included in the cache key and automatically included in requests that CloudFront sends to the origin\.
+  `all` – All query strings in viewer requests are included in the cache key and are automatically included in requests that CloudFront sends to the origin\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `all | allExcept | none | whitelist`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryStrings`  <a name="cfn-cloudfront-cachepolicy-querystringsconfig-querystrings"></a>
Contains a list of query string names\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)