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
The maximum API request rate limit over a time ranging from one to a few seconds\. The maximum API request rate limit depends on whether the underlying token bucket is at its full capacity\. For more information about request throttling, see [Manage API Request Throttling](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RateLimit`  <a name="cfn-apigateway-usageplan-throttlesettings-ratelimit"></a>
The API request steady\-state rate limit \(average requests per second over an extended period of time\)\. For more information about request throttling, see [Manage API Request Throttling](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigateway-usageplan-throttlesettings--seealso"></a>
+ [UsagePlan](https://docs.aws.amazon.com/apigateway/api-reference/resource/usage-plan/) in the *Amazon API Gateway REST API Reference*

