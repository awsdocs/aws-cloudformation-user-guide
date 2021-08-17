# AWS::ApiGateway::Deployment CanarySetting<a name="aws-properties-apigateway-deployment-canarysetting"></a>

The `CanarySetting` property type specifies settings for the canary deployment in this stage\.

`CanarySetting` is a property of the [StageDescription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-apigateway-deployment-stagedescription.html) property type\.

## Syntax<a name="aws-properties-apigateway-deployment-canarysetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-deployment-canarysetting-syntax.json"></a>

```
{
  "[PercentTraffic](#cfn-apigateway-deployment-canarysetting-percenttraffic)" : Double,
  "[StageVariableOverrides](#cfn-apigateway-deployment-canarysetting-stagevariableoverrides)" : {Key : Value, ...},
  "[UseStageCache](#cfn-apigateway-deployment-canarysetting-usestagecache)" : Boolean
}
```

### YAML<a name="aws-properties-apigateway-deployment-canarysetting-syntax.yaml"></a>

```
  [PercentTraffic](#cfn-apigateway-deployment-canarysetting-percenttraffic): Double
  [StageVariableOverrides](#cfn-apigateway-deployment-canarysetting-stagevariableoverrides): 
    Key : Value
  [UseStageCache](#cfn-apigateway-deployment-canarysetting-usestagecache): Boolean
```

## Properties<a name="aws-properties-apigateway-deployment-canarysetting-properties"></a>

`PercentTraffic`  <a name="cfn-apigateway-deployment-canarysetting-percenttraffic"></a>
The percent \(0\-100\) of traffic diverted to a canary deployment\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StageVariableOverrides`  <a name="cfn-apigateway-deployment-canarysetting-stagevariableoverrides"></a>
Stage variables overridden for a canary release deployment, including new stage variables introduced in the canary\. These stage variables are represented as a string\-to\-string map between stage variable names and their values\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseStageCache`  <a name="cfn-apigateway-deployment-canarysetting-usestagecache"></a>
Whether the canary deployment uses the stage cache or not\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigateway-deployment-canarysetting--seealso"></a>
+ [Stage](https://docs.aws.amazon.com/apigateway/api-reference/resource/stage/) in the *Amazon API Gateway REST API Reference*

