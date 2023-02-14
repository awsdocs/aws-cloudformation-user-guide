# AWS::ApiGatewayV2::ApiGatewayManagedOverrides AccessLogSettings<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-accesslogsettings"></a>

The `AccessLogSettings` property overrides the access log settings for an API Gateway\-managed stage\.

## Syntax<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-accesslogsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-accesslogsettings-syntax.json"></a>

```
{
  "[DestinationArn](#cfn-apigatewayv2-apigatewaymanagedoverrides-accesslogsettings-destinationarn)" : String,
  "[Format](#cfn-apigatewayv2-apigatewaymanagedoverrides-accesslogsettings-format)" : String
}
```

### YAML<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-accesslogsettings-syntax.yaml"></a>

```
  [DestinationArn](#cfn-apigatewayv2-apigatewaymanagedoverrides-accesslogsettings-destinationarn): String
  [Format](#cfn-apigatewayv2-apigatewaymanagedoverrides-accesslogsettings-format): String
```

## Properties<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-accesslogsettings-properties"></a>

`DestinationArn`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-accesslogsettings-destinationarn"></a>
The ARN of the CloudWatch Logs log group to receive access logs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Format`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-accesslogsettings-format"></a>
A single line format of the access logs of data, as specified by selected $context variables\. The format must include at least $context\.requestId\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)