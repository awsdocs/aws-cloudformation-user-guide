# AWS::ApiGateway::UsagePlan ThrottleSettings<a name="aws-properties-apigateway-usageplan-throttlesettings"></a>

`ThrottleSettings` is a property of the [AWS::ApiGateway::UsagePlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-usageplan.html) resource that specifies the overall request rate \(average requests per second\) and burst capacity when users call your REST APIs\.

## Syntax<a name="aws-properties-apigateway-usageplan-throttlesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-usageplan-throttlesettings-syntax.json"></a>

```
{
  "[BurstLimit](#cfn-apigateway-usageplan-throttlesettings-burstlimit)" : Integer,
  "[RateLimit](#cfn-apigateway-usageplan-throttlesettings-ratelimit)" : Double
}
```

### YAML<a name="aws-properties-apigateway-usageplan-throttlesettings-syntax.yaml"></a>

```
  [BurstLimit](#cfn-apigateway-usageplan-throttlesettings-burstlimit): Integer
  [RateLimit](#cfn-apigateway-usageplan-throttlesettings-ratelimit): Double
```

## Properties<a name="aws-properties-apigateway-usageplan-throttlesettings-properties"></a>

`BurstLimit`  <a name="cfn-apigateway-usageplan-throttlesettings-burstlimit"></a>
The API target request burst rate limit\. This allows more requests through for a period of time than the target rate limit\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RateLimit`  <a name="cfn-apigateway-usageplan-throttlesettings-ratelimit"></a>
The API target request rate limit\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigateway-usageplan-throttlesettings--seealso"></a>
+ [UsagePlan](https://docs.aws.amazon.com/apigateway/latest/api/API_UsagePlan.html) in the *Amazon API Gateway REST API Reference*

