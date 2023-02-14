# AWS::ApiGatewayV2::ApiGatewayManagedOverrides RouteSettings<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-routesettings"></a>

The `RouteSettings` property overrides the route settings for an API Gateway\-managed route\.

## Syntax<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-routesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-routesettings-syntax.json"></a>

```
{
  "[DataTraceEnabled](#cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-datatraceenabled)" : Boolean,
  "[DetailedMetricsEnabled](#cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-detailedmetricsenabled)" : Boolean,
  "[LoggingLevel](#cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-logginglevel)" : String,
  "[ThrottlingBurstLimit](#cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-throttlingburstlimit)" : Integer,
  "[ThrottlingRateLimit](#cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-throttlingratelimit)" : Double
}
```

### YAML<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-routesettings-syntax.yaml"></a>

```
  [DataTraceEnabled](#cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-datatraceenabled): Boolean
  [DetailedMetricsEnabled](#cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-detailedmetricsenabled): Boolean
  [LoggingLevel](#cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-logginglevel): String
  [ThrottlingBurstLimit](#cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-throttlingburstlimit): Integer
  [ThrottlingRateLimit](#cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-throttlingratelimit): Double
```

## Properties<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-routesettings-properties"></a>

`DataTraceEnabled`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-datatraceenabled"></a>
Specifies whether \(`true`\) or not \(`false`\) data trace logging is enabled for this route\. This property affects the log entries pushed to Amazon CloudWatch Logs\. Supported only for WebSocket APIs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DetailedMetricsEnabled`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-detailedmetricsenabled"></a>
Specifies whether detailed metrics are enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingLevel`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-logginglevel"></a>
Specifies the logging level for this route: `INFO`, `ERROR`, or `OFF`\. This property affects the log entries pushed to Amazon CloudWatch Logs\. Supported only for WebSocket APIs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThrottlingBurstLimit`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-throttlingburstlimit"></a>
Specifies the throttling burst limit\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThrottlingRateLimit`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-routesettings-throttlingratelimit"></a>
Specifies the throttling rate limit\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)