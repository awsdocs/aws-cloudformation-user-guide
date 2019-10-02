# AWS::ApiGatewayV2::Stage AccessLogSettings<a name="aws-properties-apigatewayv2-stage-accesslogsettings"></a>

Settings for logging access in a stage\.

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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Format`  <a name="cfn-apigatewayv2-stage-accesslogsettings-format"></a>
A single line format of the access logs of data, as specified by selected $context variables\. The format must include at least $context\.requestId\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-apigatewayv2-stage-accesslogsettings--seealso"></a>
+ [Stages](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/apis-apiid-stages.html) in the *Amazon API Gateway Version 2 API Reference*

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-east-1`
- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-gov-east-1`
- `us-gov-west-1`
- `us-west-1`
- `us-west-2`
