# Amazon API Gateway UsagePlan QuotaSettings<a name="aws-properties-apigateway-usageplan-quotasettings"></a>

`QuotaSettings` is a property of the [AWS::ApiGateway::UsagePlan](aws-resource-apigateway-usageplan.md) resource that specifies the maximum number of requests users can make to your Amazon API Gateway \(API Gateway\) APIs\.

## Syntax<a name="aws-properties-apigateway-usageplan-quotasettings-syntax"></a>

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

`Offset`  <a name="cfn-apigateway-usageplan-quotasettings-offset"></a>
For the initial time period, the number of requests to subtract from the specified limit\. When you first implement a usage plan, the plan might start in the middle of the week or month\. With this property, you can decrease the limit for this initial time period\.  
*Required*: No  
*Type*: Integer

`Period`  <a name="cfn-apigateway-usageplan-quotasettings-period"></a>
The time period for which the maximum limit of requests applies, such as `DAY` or `WEEK`\. For valid values, see the `period` property for the [UsagePlan](http://docs.aws.amazon.com/apigateway/api-reference/resource/usage-plan) resource in the *Amazon API Gateway REST API Reference*\.  
*Required*: No  
*Type*: String