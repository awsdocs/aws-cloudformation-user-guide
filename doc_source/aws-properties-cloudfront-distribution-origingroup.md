# AWS::CloudFront::Distribution OriginGroup<a name="aws-properties-cloudfront-distribution-origingroup"></a>

An origin group includes two origins \(a primary origin and a second origin to failover to\) and a failover criteria that you specify\. You create an origin group to support origin failover in CloudFront\. When you create or update a distribution, you can specifiy the origin group instead of a single origin, and CloudFront will failover from the primary origin to the second origin under the failover conditions that you've chosen\.

## Syntax<a name="aws-properties-cloudfront-distribution-origingroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-distribution-origingroup-syntax.json"></a>

```
{
  "[FailoverCriteria](#cfn-cloudfront-distribution-origingroup-failovercriteria)" : OriginGroupFailoverCriteria,
  "[Id](#cfn-cloudfront-distribution-origingroup-id)" : String,
  "[Members](#cfn-cloudfront-distribution-origingroup-members)" : OriginGroupMembers
}
```

### YAML<a name="aws-properties-cloudfront-distribution-origingroup-syntax.yaml"></a>

```
  [FailoverCriteria](#cfn-cloudfront-distribution-origingroup-failovercriteria): 
    OriginGroupFailoverCriteria
  [Id](#cfn-cloudfront-distribution-origingroup-id): String
  [Members](#cfn-cloudfront-distribution-origingroup-members): 
    OriginGroupMembers
```

## Properties<a name="aws-properties-cloudfront-distribution-origingroup-properties"></a>

`FailoverCriteria`  <a name="cfn-cloudfront-distribution-origingroup-failovercriteria"></a>
A complex type that contains information about the failover criteria for an origin group\.  
*Required*: Yes  
*Type*: [OriginGroupFailoverCriteria](aws-properties-cloudfront-distribution-origingroupfailovercriteria.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-cloudfront-distribution-origingroup-id"></a>
The origin group's ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Members`  <a name="cfn-cloudfront-distribution-origingroup-members"></a>
A complex type that contains information about the origins in an origin group\.  
*Required*: Yes  
*Type*: [OriginGroupMembers](aws-properties-cloudfront-distribution-origingroupmembers.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)