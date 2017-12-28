# Amazon API Gateway UsagePlan ThrottleSettings<a name="aws-properties-apigateway-usageplan-throttlesettings"></a>

`ThrottleSettings` is a property of the [AWS::ApiGateway::UsagePlan](aws-resource-apigateway-usageplan.md) resource that specifies the overall request rate \(average requests per second\) and burst capacity when users call your Amazon API Gateway \(API Gateway\) APIs\.

## Syntax<a name="aws-properties-apigateway-usageplan-throttlesettings-syntax"></a>

### JSON<a name="aws-properties-apigateway-usageplan-throttlesettings-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-usageplan-throttlesettings-burstlimit)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-usageplan-throttlesettings-ratelimit)" : Number
}
```

### YAML<a name="aws-properties-apigateway-usageplan-throttlesettings-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-usageplan-throttlesettings-burstlimit): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-usageplan-throttlesettings-ratelimit): Number
```

## Properties<a name="aws-properties-apigateway-usageplan-throttlesettings-properties"></a>

`BurstLimit`  
The maximum API request rate limit over a time ranging from one to a few seconds\. The maximum API request rate limit depends on whether the underlying token bucket is at its full capacity\. For more information about request throttling, see [Manage API Request Throttling](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html) in the *API Gateway Developer Guide*\.  
*Required: *No  
*Type*: Integer

`RateLimit`  
The API request steady\-state rate limit \(average requests per second over an extended period of time\)\. For more information about request throttling, see [Manage API Request Throttling](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html) in the *API Gateway Developer Guide*\.  
*Required: *No  
*Type*: Number