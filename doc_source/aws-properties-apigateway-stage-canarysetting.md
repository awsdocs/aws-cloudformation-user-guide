# AWS::ApiGateway::Stage CanarySetting<a name="aws-properties-apigateway-stage-canarysetting"></a>

The `CanarySetting` property type specifies settings for the canary deployment in this stage\.

`CanarySetting` is a property of the [AWS::ApiGateway::Stage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-stage.html) resource\.

## Syntax<a name="aws-properties-apigateway-stage-canarysetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-stage-canarysetting-syntax.json"></a>

```
{
  "[DeploymentId](#cfn-apigateway-stage-canarysetting-deploymentid)" : String,
  "[PercentTraffic](#cfn-apigateway-stage-canarysetting-percenttraffic)" : Double,
  "[StageVariableOverrides](#cfn-apigateway-stage-canarysetting-stagevariableoverrides)" : {Key : Value, ...},
  "[UseStageCache](#cfn-apigateway-stage-canarysetting-usestagecache)" : Boolean
}
```

### YAML<a name="aws-properties-apigateway-stage-canarysetting-syntax.yaml"></a>

```
  [DeploymentId](#cfn-apigateway-stage-canarysetting-deploymentid): String
  [PercentTraffic](#cfn-apigateway-stage-canarysetting-percenttraffic): Double
  [StageVariableOverrides](#cfn-apigateway-stage-canarysetting-stagevariableoverrides): 
    Key : Value
  [UseStageCache](#cfn-apigateway-stage-canarysetting-usestagecache): Boolean
```

## Properties<a name="aws-properties-apigateway-stage-canarysetting-properties"></a>

`DeploymentId`  <a name="cfn-apigateway-stage-canarysetting-deploymentid"></a>
The identifier of the deployment that the stage points to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PercentTraffic`  <a name="cfn-apigateway-stage-canarysetting-percenttraffic"></a>
The percentage \(0\-100\) of traffic diverted to a canary deployment\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StageVariableOverrides`  <a name="cfn-apigateway-stage-canarysetting-stagevariableoverrides"></a>
Stage variables overridden for a canary release deployment, including new stage variables introduced in the canary\. These stage variables are represented as a string\-to\-string map between stage variable names and their values\.  
Duplicates are not allowed\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseStageCache`  <a name="cfn-apigateway-stage-canarysetting-usestagecache"></a>
Whether the canary deployment uses the stage cache or not\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigateway-stage-canarysetting--seealso"></a>
+ [Stage](https://docs.aws.amazon.com/apigateway/api-reference/resource/stage/) in the *Amazon API Gateway REST API Reference*

