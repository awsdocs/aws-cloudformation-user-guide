# AWS::ApiGatewayV2::Stage RouteSettings<a name="aws-properties-apigatewayv2-stage-routesettings"></a>

Represents a collection of route settings\.

## Syntax<a name="aws-properties-apigatewayv2-stage-routesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigatewayv2-stage-routesettings-syntax.json"></a>

```
{
  "[DataTraceEnabled](#cfn-apigatewayv2-stage-routesettings-datatraceenabled)" : Boolean,
  "[DetailedMetricsEnabled](#cfn-apigatewayv2-stage-routesettings-detailedmetricsenabled)" : Boolean,
  "[LoggingLevel](#cfn-apigatewayv2-stage-routesettings-logginglevel)" : String,
  "[ThrottlingBurstLimit](#cfn-apigatewayv2-stage-routesettings-throttlingburstlimit)" : Integer,
  "[ThrottlingRateLimit](#cfn-apigatewayv2-stage-routesettings-throttlingratelimit)" : Double
}
```

### YAML<a name="aws-properties-apigatewayv2-stage-routesettings-syntax.yaml"></a>

```
  [DataTraceEnabled](#cfn-apigatewayv2-stage-routesettings-datatraceenabled): Boolean
  [DetailedMetricsEnabled](#cfn-apigatewayv2-stage-routesettings-detailedmetricsenabled): Boolean
  [LoggingLevel](#cfn-apigatewayv2-stage-routesettings-logginglevel): String
  [ThrottlingBurstLimit](#cfn-apigatewayv2-stage-routesettings-throttlingburstlimit): Integer
  [ThrottlingRateLimit](#cfn-apigatewayv2-stage-routesettings-throttlingratelimit): Double
```

## Properties<a name="aws-properties-apigatewayv2-stage-routesettings-properties"></a>

`DataTraceEnabled`  <a name="cfn-apigatewayv2-stage-routesettings-datatraceenabled"></a>
Specifies whether \(`true`\) or not \(`false`\) data trace logging is enabled for this route\. This property affects the log entries pushed to Amazon CloudWatch Logs\. Supported only for WebSocket APIs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DetailedMetricsEnabled`  <a name="cfn-apigatewayv2-stage-routesettings-detailedmetricsenabled"></a>
Specifies whether detailed metrics are enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingLevel`  <a name="cfn-apigatewayv2-stage-routesettings-logginglevel"></a>
Specifies the logging level for this route: `INFO`, `ERROR`, or `OFF`\. This property affects the log entries pushed to Amazon CloudWatch Logs\. Supported only for WebSocket APIs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThrottlingBurstLimit`  <a name="cfn-apigatewayv2-stage-routesettings-throttlingburstlimit"></a>
Specifies the throttling burst limit\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThrottlingRateLimit`  <a name="cfn-apigatewayv2-stage-routesettings-throttlingratelimit"></a>
Specifies the throttling rate limit\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigatewayv2-stage-routesettings--seealso"></a>
+ [Stages](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/apis-apiid-stages.html) in the *Amazon API Gateway Version 2 API Reference*

