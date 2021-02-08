# AWS::ApiGateway::UsagePlan QuotaSettings<a name="aws-properties-apigateway-usageplan-quotasettings"></a>

`QuotaSettings` is a property of the [AWS::ApiGateway::UsagePlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-usageplan.html) resource that specifies the maximum number of requests users can make to your REST APIs\.

## Syntax<a name="aws-properties-apigateway-usageplan-quotasettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-usageplan-quotasettings-syntax.json"></a>

```
{
  "[Limit](#cfn-apigateway-usageplan-quotasettings-limit)" : Integer,
  "[Offset](#cfn-apigateway-usageplan-quotasettings-offset)" : Integer,
  "[Period](#cfn-apigateway-usageplan-quotasettings-period)" : String
}
```

### YAML<a name="aws-properties-apigateway-usageplan-quotasettings-syntax.yaml"></a>

```
  [Limit](#cfn-apigateway-usageplan-quotasettings-limit): Integer
  [Offset](#cfn-apigateway-usageplan-quotasettings-offset): Integer
  [Period](#cfn-apigateway-usageplan-quotasettings-period): String
```

## Properties<a name="aws-properties-apigateway-usageplan-quotasettings-properties"></a>

`Limit`  <a name="cfn-apigateway-usageplan-quotasettings-limit"></a>
The maximum number of requests that users can make within the specified time period\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Offset`  <a name="cfn-apigateway-usageplan-quotasettings-offset"></a>
The day that a time period starts\. For example, with a time period of `WEEK`, an offset of `0` starts on Sunday, and an offset of `1` starts on Monday\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Period`  <a name="cfn-apigateway-usageplan-quotasettings-period"></a>
The time period for which the maximum limit of requests applies, such as `DAY` or `WEEK`\. For valid values, see the period property for the [UsagePlan](https://docs.aws.amazon.com/apigateway/api-reference/resource/usage-plan) resource in the *Amazon API Gateway REST API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigateway-usageplan-quotasettings--seealso"></a>
+ [UsagePlan](https://docs.aws.amazon.com/apigateway/api-reference/resource/usage-plan/) in the *Amazon API Gateway REST API Reference*

