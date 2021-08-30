# AWS::CloudFront::Distribution OriginGroupMember<a name="aws-properties-cloudfront-distribution-origingroupmember"></a>

An origin in an origin group\.

## Syntax<a name="aws-properties-cloudfront-distribution-origingroupmember-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-distribution-origingroupmember-syntax.json"></a>

```
{
  "[OriginId](#cfn-cloudfront-distribution-origingroupmember-originid)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distribution-origingroupmember-syntax.yaml"></a>

```
  [OriginId](#cfn-cloudfront-distribution-origingroupmember-originid): String
```

## Properties<a name="aws-properties-cloudfront-distribution-origingroupmember-properties"></a>

`OriginId`  <a name="cfn-cloudfront-distribution-origingroupmember-originid"></a>
The ID for an origin in an origin group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)