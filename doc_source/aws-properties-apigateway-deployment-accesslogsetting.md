# AWS::ApiGateway::Deployment AccessLogSetting<a name="aws-properties-apigateway-deployment-accesslogsetting"></a>

The `AccessLogSetting` property type specifies settings for logging access in this stage\.

 `AccessLogSetting` is a property of the [StageDescription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-apigateway-deployment-stagedescription.html) property type\.

## Syntax<a name="aws-properties-apigateway-deployment-accesslogsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-deployment-accesslogsetting-syntax.json"></a>

```
{
  "[DestinationArn](#cfn-apigateway-deployment-accesslogsetting-destinationarn)" : String,
  "[Format](#cfn-apigateway-deployment-accesslogsetting-format)" : String
}
```

### YAML<a name="aws-properties-apigateway-deployment-accesslogsetting-syntax.yaml"></a>

```
  [DestinationArn](#cfn-apigateway-deployment-accesslogsetting-destinationarn): String
  [Format](#cfn-apigateway-deployment-accesslogsetting-format): String
```

## Properties<a name="aws-properties-apigateway-deployment-accesslogsetting-properties"></a>

`DestinationArn`  <a name="cfn-apigateway-deployment-accesslogsetting-destinationarn"></a>
The Amazon Resource Name \(ARN\) of the CloudWatch Logs log group or Kinesis Data Firehose delivery stream to receive access logs\. If you specify a Kinesis Data Firehose delivery stream, the stream name must begin with `amazon-apigateway-`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Format`  <a name="cfn-apigateway-deployment-accesslogsetting-format"></a>
A single line format of the access logs of data, as specified by selected [$context variables](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-mapping-template-reference.html#context-variable-reference)\. The format must include at least `$context.requestId`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigateway-deployment-accesslogsetting--seealso"></a>
+ [accessLogSettings](https://docs.aws.amazon.com/apigateway/api-reference/resource/stage/#accessLogSettings) in the *Amazon API Gateway REST API Reference*

