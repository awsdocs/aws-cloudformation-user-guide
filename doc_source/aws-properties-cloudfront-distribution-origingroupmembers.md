# AWS::CloudFront::Distribution OriginGroupMembers<a name="aws-properties-cloudfront-distribution-origingroupmembers"></a>

A complex data type for the origins included in an origin group\.

## Syntax<a name="aws-properties-cloudfront-distribution-origingroupmembers-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-distribution-origingroupmembers-syntax.json"></a>

```
{
  "[Items](#cfn-cloudfront-distribution-origingroupmembers-items)" : [ OriginGroupMember, ... ],
  "[Quantity](#cfn-cloudfront-distribution-origingroupmembers-quantity)" : Integer
}
```

### YAML<a name="aws-properties-cloudfront-distribution-origingroupmembers-syntax.yaml"></a>

```
  [Items](#cfn-cloudfront-distribution-origingroupmembers-items): 
    - OriginGroupMember
  [Quantity](#cfn-cloudfront-distribution-origingroupmembers-quantity): Integer
```

## Properties<a name="aws-properties-cloudfront-distribution-origingroupmembers-properties"></a>

`Items`  <a name="cfn-cloudfront-distribution-origingroupmembers-items"></a>
Items \(origins\) in an origin group\.  
*Required*: Yes  
*Type*: List of [OriginGroupMember](aws-properties-cloudfront-distribution-origingroupmember.md)  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Quantity`  <a name="cfn-cloudfront-distribution-origingroupmembers-quantity"></a>
The number of origins in an origin group\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)