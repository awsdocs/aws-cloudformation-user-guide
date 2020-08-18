# AWS::ApiGatewayV2::ApiGatewayManagedOverrides StageOverrides<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-stageoverrides"></a>

The `StageOverrides` property overrides the stage configuration for an API Gateway\-managed stage\. If you remove this property, API Gateway restores the default values\.

## Syntax<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-syntax.json"></a>

```
{
  "[AccessLogSettings](#cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-accesslogsettings)" : AccessLogSettings,
  "[AutoDeploy](#cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-autodeploy)" : Boolean,
  "[DefaultRouteSettings](#cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-defaultroutesettings)" : RouteSettings,
  "[Description](#cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-description)" : String,
  "[RouteSettings](#cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-routesettings)" : Json,
  "[StageVariables](#cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-stagevariables)" : Json
}
```

### YAML<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-syntax.yaml"></a>

```
  [AccessLogSettings](#cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-accesslogsettings): 
    AccessLogSettings
  [AutoDeploy](#cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-autodeploy): Boolean
  [DefaultRouteSettings](#cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-defaultroutesettings): 
    RouteSettings
  [Description](#cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-description): String
  [RouteSettings](#cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-routesettings): Json
  [StageVariables](#cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-stagevariables): Json
```

## Properties<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-properties"></a>

`AccessLogSettings`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-accesslogsettings"></a>
Settings for logging access in a stage\.  
*Required*: No  
*Type*: [AccessLogSettings](aws-properties-apigatewayv2-apigatewaymanagedoverrides-accesslogsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoDeploy`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-autodeploy"></a>
Specifies whether updates to an API automatically trigger a new deployment\. The default value is `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultRouteSettings`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-defaultroutesettings"></a>
The default route settings for the stage\.  
*Required*: No  
*Type*: [RouteSettings](aws-properties-apigatewayv2-apigatewaymanagedoverrides-routesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-description"></a>
The description for the API stage\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RouteSettings`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-routesettings"></a>
Route settings for the stage\.  
*Required*: No  
*Type*: [Json](aws-properties-apigatewayv2-apigatewaymanagedoverrides-routesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StageVariables`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-stageoverrides-stagevariables"></a>
A map that defines the stage variables for a `Stage`\. Variable names can have alphanumeric and underscore characters, and the values must match \[A\-Za\-z0\-9\-\.\_\~:/?\#&=,\]\+\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)