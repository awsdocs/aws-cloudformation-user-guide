# Amazon API Gateway Deployment DeploymentCanarySettings<a name="aws-properties-apigateway-deployment-deploymentcanarysettings"></a>

<a name="aws-properties-apigateway-deployment-deploymentcanarysettings-description"></a>The `DeploymentCanarySettings` property type specifies settings for the canary deployment\.

<a name="aws-properties-apigateway-deployment-deploymentcanarysettings-inheritance"></a> `DeploymentCanarySettings` is a property of the [AWS::ApiGateway::Deployment](aws-resource-apigateway-deployment.md) resource\.

## Syntax<a name="aws-properties-apigateway-deployment-deploymentcanarysettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-deployment-deploymentcanarysettings-syntax.json"></a>

```
{
  "[PercentTraffic](#cfn-apigateway-deployment-deploymentcanarysettings-percenttraffic)" : Double ,
  "[StageVariableOverrides](#cfn-apigateway-deployment-deploymentcanarysettings-stagevariableoverrides)" : { String:String, ... },
  "[UseStageCache](#cfn-apigateway-deployment-deploymentcanarysettings-usestagecache)" : Boolean
}
```

### YAML<a name="aws-properties-apigateway-deployment-deploymentcanarysettings-syntax.yaml"></a>

```
[PercentTraffic](#cfn-apigateway-deployment-deploymentcanarysettings-percenttraffic): Double
[StageVariableOverrides](#cfn-apigateway-deployment-deploymentcanarysettings-stagevariableoverrides): String: String
[UseStageCache](#cfn-apigateway-deployment-deploymentcanarysettings-usestagecache): Boolean
```

## Properties<a name="aws-properties-apigateway-deployment-deploymentcanarysettings-properties"></a>

`PercentTraffic`  <a name="cfn-apigateway-deployment-deploymentcanarysettings-percenttraffic"></a>
The percent \(0\-100\) of traffic diverted to a canary deployment\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`StageVariableOverrides`  <a name="cfn-apigateway-deployment-deploymentcanarysettings-stagevariableoverrides"></a>
Stage variables overridden for a canary release deployment, including new stage variables introduced in the canary\. These stage variables are represented as a string\-to\-string map between stage variable names and their values\.  
Duplicates are not allowed\.  
*Required*: No  
*Type*: String to String map  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`UseStageCache`  <a name="cfn-apigateway-deployment-deploymentcanarysettings-usestagecache"></a>
Whether the canary deployment uses the stage cache or not\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## See Also<a name="aws-properties-apigateway-deployment-deploymentcanarysettings-seealso"></a>
+ [Deployment](https://docs.aws.amazon.com/apigateway/api-reference/resource/deployment/) in the *API Gateway API Reference*