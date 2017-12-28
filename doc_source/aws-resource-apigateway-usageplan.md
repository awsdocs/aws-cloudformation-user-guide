# AWS::ApiGateway::UsagePlan<a name="aws-resource-apigateway-usageplan"></a>

The `AWS::ApiGateway::UsagePlan` resource specifies a usage plan for deployed Amazon API Gateway \(API Gateway\) APIs\. A usage plan enforces throttling and quota limits on individual client API keys\. For more information, see [Creating and Using API Usage Plans in Amazon API Gateway](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-api-usage-plans.html) in the *API Gateway Developer Guide*\.


+ [Syntax](#aws-resource-apigateway-usageplan-syntax)
+ [Properties](#aws-resource-apigateway-usageplan-properties)
+ [Return Value](#aws-resource-apigateway-usageplan-returnvalues)
+ [Examples](#aws-resource-apigateway-usageplan-examples)

## Syntax<a name="aws-resource-apigateway-usageplan-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-usageplan-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::UsagePlan",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-usageplan-apistages)" : [ ApiStage, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-usageplan-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-usageplan-quota)" : QuotaSettings,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-usageplan-throttle)" : ThrottleSettings,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-usageplan-usageplanname)" : String
  }
}
```

### YAML<a name="aws-resource-apigateway-usageplan-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::UsagePlan"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-usageplan-apistages): 
  - ApiStage
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-usageplan-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-usageplan-quota): QuotaSettings
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-usageplan-throttle): ThrottleSettings
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-usageplan-usageplanname): String
```

## Properties<a name="aws-resource-apigateway-usageplan-properties"></a>

`ApiStages`  
The API stages to associate with this usage plan\.  
*Required: *No  
*Type*: List of [Amazon API Gateway UsagePlan ApiStage](aws-properties-apigateway-usageplan-apistage.md)  
*Update requires*: No interruption

`Description`  
The purpose of this usage plan\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`Quota`  
Configures the number of requests that users can make within a given interval\.  
*Required: *No  
*Type*: [Amazon API Gateway UsagePlan QuotaSettings](aws-properties-apigateway-usageplan-quotasettings.md)  
*Update requires*: No interruption

`Throttle`  
Configures the overall request rate \(average requests per second\) and burst capacity\.  
*Required: *No  
*Type*: [Amazon API Gateway UsagePlan ThrottleSettings](aws-properties-apigateway-usageplan-throttlesettings.md)  
*Update requires*: No interruption

`UsagePlanName`  
A name for this usage plan\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

## Return Value<a name="aws-resource-apigateway-usageplan-returnvalues"></a>

### Ref<a name="w3ab2c21c10c85c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the usage plan ID, such as `MyUsagePlan`\.

For more information about using the `Ref` function, see Ref\.

## Examples<a name="aws-resource-apigateway-usageplan-examples"></a>

The following examples create a usage plan for the `Prod` API stage, with a quota of 5000 requests per month and a rate limit of 100 requests per second\.

### JSON<a name="aws-resource-apigateway-usageplan-example.json"></a>

```
"usagePlan" : {
  "Type" : "AWS::ApiGateway::UsagePlan",
  "Properties" : {
    "ApiStages" : [ {"ApiId" : { "Ref" : "MyRestApi" }, "Stage" : { "Ref" : "Prod" }} ],
    "Description" : "Customer ABC's usage plan",
    "Quota" : {
      "Limit" : 5000,
      "Period" : "MONTH"
    },
    "Throttle" : {
      "BurstLimit" : 200,
      "RateLimit" : 100
    },
    "UsagePlanName" : "Plan_ABC"
  }
}
```

### YAML<a name="aws-resource-apigateway-usageplan-example.yaml"></a>

```
usagePlan:
  Type: AWS::ApiGateway::UsagePlan
  Properties:
    ApiStages:
    - ApiId: !Ref 'MyRestApi'
      Stage: !Ref 'Prod'
    Description: Customer ABC's usage plan
    Quota:
      Limit: 5000
      Period: MONTH
    Throttle:
      BurstLimit: 200
      RateLimit: 100
    UsagePlanName: Plan_ABC
```