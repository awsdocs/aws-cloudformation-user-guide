# Amazon API Gateway Stage AccessLogSetting<a name="aws-properties-apigateway-stage-accesslogsetting"></a>

<a name="aws-properties-apigateway-stage-accesslogsetting-description"></a>The `AccessLogSetting` property type specifies settings for logging access in this stage\.

<a name="aws-properties-apigateway-stage-accesslogsetting-inheritance"></a> `AccessLogSetting` is a property of the [AWS::ApiGateway::Stage](aws-resource-apigateway-stage.md) resource\.

## Syntax<a name="aws-properties-apigateway-stage-accesslogsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-stage-accesslogsetting-syntax.json"></a>

```
{
  "[DestinationArn](#cfn-apigateway-stage-accesslogsetting-destinationarn)" : String,
  "[Format](#cfn-apigateway-stage-accesslogsetting-format)" : String
}
```

### YAML<a name="aws-properties-apigateway-stage-accesslogsetting-syntax.yaml"></a>

```
[DestinationArn](#cfn-apigateway-stage-accesslogsetting-destinationarn): String
[Format](#cfn-apigateway-stage-accesslogsetting-format): String
```

## Properties<a name="aws-properties-apigateway-stage-accesslogsetting-properties"></a>

`DestinationArn`  <a name="cfn-apigateway-stage-accesslogsetting-destinationarn"></a>
The Amazon Resource Name \(ARN\) of the CloudWatch Logs log group to receive access logs  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Format`  <a name="cfn-apigateway-stage-accesslogsetting-format"></a>
A single line format of the access logs of data, as specified by selected [$context variables](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-mapping-template-reference.html#context-variable-reference)\. The format must include at least `$context.requestId`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-apigateway-stage-accesslogsetting-seealso"></a>
+ [accessLogSettings](https://docs.aws.amazon.com/apigateway/api-reference/resource/stage/#accessLogSettings) in the *API Gateway API Reference*