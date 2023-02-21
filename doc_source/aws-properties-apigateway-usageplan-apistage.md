# AWS::ApiGateway::UsagePlan ApiStage<a name="aws-properties-apigateway-usageplan-apistage"></a>

API stage name of the associated API stage in a usage plan\.

## Syntax<a name="aws-properties-apigateway-usageplan-apistage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-usageplan-apistage-syntax.json"></a>

```
{
  "[ApiId](#cfn-apigateway-usageplan-apistage-apiid)" : String,
  "[Stage](#cfn-apigateway-usageplan-apistage-stage)" : String,
  "[Throttle](#cfn-apigateway-usageplan-apistage-throttle)" : {Key : Value, ...}
}
```

### YAML<a name="aws-properties-apigateway-usageplan-apistage-syntax.yaml"></a>

```
  [ApiId](#cfn-apigateway-usageplan-apistage-apiid): String
  [Stage](#cfn-apigateway-usageplan-apistage-stage): String
  [Throttle](#cfn-apigateway-usageplan-apistage-throttle): 
    Key : Value
```

## Properties<a name="aws-properties-apigateway-usageplan-apistage-properties"></a>

`ApiId`  <a name="cfn-apigateway-usageplan-apistage-apiid"></a>
API Id of the associated API stage in a usage plan\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Stage`  <a name="cfn-apigateway-usageplan-apistage-stage"></a>
API stage name of the associated API stage in a usage plan\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Throttle`  <a name="cfn-apigateway-usageplan-apistage-throttle"></a>
Map containing method level throttling information for API stage in a usage plan\.  
*Required*: No  
*Type*: Map of [ThrottleSettings](aws-properties-apigateway-usageplan-throttlesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigateway-usageplan-apistage--seealso"></a>
+ [UsagePlan](https://docs.aws.amazon.com/apigateway/latest/api/API_UsagePlan.html) in the *Amazon API Gateway REST API Reference*

