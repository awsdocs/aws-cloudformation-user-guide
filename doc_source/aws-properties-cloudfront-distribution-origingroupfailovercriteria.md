# AWS::CloudFront::Distribution OriginGroupFailoverCriteria<a name="aws-properties-cloudfront-distribution-origingroupfailovercriteria"></a>

A complex data type that includes information about the failover criteria for an origin group, including the status codes for which CloudFront will failover from the primary origin to the second origin\.

## Syntax<a name="aws-properties-cloudfront-distribution-origingroupfailovercriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-distribution-origingroupfailovercriteria-syntax.json"></a>

```
{
  "[StatusCodes](#cfn-cloudfront-distribution-origingroupfailovercriteria-statuscodes)" : StatusCodes
}
```

### YAML<a name="aws-properties-cloudfront-distribution-origingroupfailovercriteria-syntax.yaml"></a>

```
  [StatusCodes](#cfn-cloudfront-distribution-origingroupfailovercriteria-statuscodes): 
    StatusCodes
```

## Properties<a name="aws-properties-cloudfront-distribution-origingroupfailovercriteria-properties"></a>

`StatusCodes`  <a name="cfn-cloudfront-distribution-origingroupfailovercriteria-statuscodes"></a>
The status codes that, when returned from the primary origin, will trigger CloudFront to failover to the second origin\.  
*Required*: Yes  
*Type*: [StatusCodes](aws-properties-cloudfront-distribution-statuscodes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)