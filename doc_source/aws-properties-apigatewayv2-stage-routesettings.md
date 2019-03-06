# RouteSettings<a name="aws-properties-apigatewayv2-stage-routesettings"></a>

<a name="aws-properties-apigatewayv2-stage-routesettings-description"></a>The `RouteSettings` property type is a mapping of `RouteId` to `RouteSettings` that specifies route settings for an API Gateway stage\.

<a name="aws-properties-apigatewayv2-stage-routesettings-inheritance"></a> `RouteSettings` is a property of the [AWS::ApiGatewayV2::Stage](aws-resource-apigatewayv2-stage.md) resource\.

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
Specifies whether \(true\) or not \(false\) data trace logging is enabled for this route\. This property affects the log entries pushed to Amazon CloudWatch Logs\.   
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DetailedMetricsEnabled`  <a name="cfn-apigatewayv2-stage-routesettings-detailedmetricsenabled"></a>
Specifies whether detailed metrics are enabled\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LoggingLevel`  <a name="cfn-apigatewayv2-stage-routesettings-logginglevel"></a>
Specifies the logging level for this route: DEBUG, INFO, or WARN\. This property affects the log entries pushed to Amazon CloudWatch Logs\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ThrottlingBurstLimit`  <a name="cfn-apigatewayv2-stage-routesettings-throttlingburstlimit"></a>
Specifies the throttling burst limit\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ThrottlingRateLimit`  <a name="cfn-apigatewayv2-stage-routesettings-throttlingratelimit"></a>
Specifies the throttling rate limit\.  
 *Required*: No  
 *Type*: Double  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-apigatewayv2-stage-routesettings-seealso"></a>
+  [RouteSettings](https://docs.aws.amazon.com//apigatewayv2/latest/api-reference/apis-apiid-stages-stagename.html#apis-apiid-stages-stagename-model-routesettings) in the *Amazon API Gateway V2 API Reference* 