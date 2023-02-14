# AWS::CloudFront::OriginRequestPolicy QueryStringsConfig<a name="aws-properties-cloudfront-originrequestpolicy-querystringsconfig"></a>

An object that determines whether any URL query strings in viewer requests \(and if so, which query strings\) are included in requests that CloudFront sends to the origin\.

## Syntax<a name="aws-properties-cloudfront-originrequestpolicy-querystringsconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-originrequestpolicy-querystringsconfig-syntax.json"></a>

```
{
  "[QueryStringBehavior](#cfn-cloudfront-originrequestpolicy-querystringsconfig-querystringbehavior)" : String,
  "[QueryStrings](#cfn-cloudfront-originrequestpolicy-querystringsconfig-querystrings)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudfront-originrequestpolicy-querystringsconfig-syntax.yaml"></a>

```
  [QueryStringBehavior](#cfn-cloudfront-originrequestpolicy-querystringsconfig-querystringbehavior): 
    String
  [QueryStrings](#cfn-cloudfront-originrequestpolicy-querystringsconfig-querystrings): 
    - String
```

## Properties<a name="aws-properties-cloudfront-originrequestpolicy-querystringsconfig-properties"></a>

`QueryStringBehavior`  <a name="cfn-cloudfront-originrequestpolicy-querystringsconfig-querystringbehavior"></a>
Determines whether any URL query strings in viewer requests are included in requests that CloudFront sends to the origin\. Valid values are:  
+  `none` – Query strings in viewer requests are not included in requests that CloudFront sends to the origin\. Even when this field is set to `none`, any query strings that are listed in a `CachePolicy` *are* included in origin requests\.
+  `whitelist` – The query strings in viewer requests that are listed in the `QueryStringNames` type are included in requests that CloudFront sends to the origin\.
+  `all` – All query strings in viewer requests are included in requests that CloudFront sends to the origin\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `all | none | whitelist`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryStrings`  <a name="cfn-cloudfront-originrequestpolicy-querystringsconfig-querystrings"></a>
Contains a list of query string names\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)