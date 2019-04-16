# AccessLogSettings<a name="aws-properties-apigatewayv2-stage-accesslogsettings"></a>

<a name="aws-properties-apigatewayv2-stage-accesslogsettings-description"></a>The `AccessLogSettings` property type specifies access log settings for an API Gateway stage\.

<a name="aws-properties-apigatewayv2-stage-accesslogsettings-inheritance"></a> `AccessLogSettings` is a property of the [AWS::ApiGatewayV2::Stage](aws-resource-apigatewayv2-stage.md) resource\.

## Syntax<a name="aws-properties-apigatewayv2-stage-accesslogsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigatewayv2-stage-accesslogsettings-syntax.json"></a>

```
{
  "[DestinationArn](#cfn-apigatewayv2-stage-accesslogsettings-destinationarn)" : String,
  "[Format](#cfn-apigatewayv2-stage-accesslogsettings-format)" : String
}
```

### YAML<a name="aws-properties-apigatewayv2-stage-accesslogsettings-syntax.yaml"></a>

```
[DestinationArn](#cfn-apigatewayv2-stage-accesslogsettings-destinationarn): String
[Format](#cfn-apigatewayv2-stage-accesslogsettings-format): String
```

## Properties<a name="aws-properties-apigatewayv2-stage-accesslogsettings-properties"></a>

`DestinationArn`  <a name="cfn-apigatewayv2-stage-accesslogsettings-destinationarn"></a>
The ARN of the CloudWatch Logs log group to receive access logs\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Format`  <a name="cfn-apigatewayv2-stage-accesslogsettings-format"></a>
A single line format of the access logs of data, as specified by selected `$context` variables\. The format must include at least `$context.requestId`\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-apigatewayv2-stage-accesslogsettings-seealso"></a>
+  [AccessLogSettings](https://docs.aws.amazon.com//apigatewayv2/latest/api-reference/apis-apiid-stages-stagename.html#apis-apiid-stages-stagename-model-accesslogsettings) in the *Amazon API Gateway V2 API Reference* 