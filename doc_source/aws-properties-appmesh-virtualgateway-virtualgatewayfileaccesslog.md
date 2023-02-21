# AWS::AppMesh::VirtualGateway VirtualGatewayFileAccessLog<a name="aws-properties-appmesh-virtualgateway-virtualgatewayfileaccesslog"></a>

An object that represents an access log file\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewayfileaccesslog-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewayfileaccesslog-syntax.json"></a>

```
{
  "[Format](#cfn-appmesh-virtualgateway-virtualgatewayfileaccesslog-format)" : LoggingFormat,
  "[Path](#cfn-appmesh-virtualgateway-virtualgatewayfileaccesslog-path)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewayfileaccesslog-syntax.yaml"></a>

```
  [Format](#cfn-appmesh-virtualgateway-virtualgatewayfileaccesslog-format): 
    LoggingFormat
  [Path](#cfn-appmesh-virtualgateway-virtualgatewayfileaccesslog-path): String
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewayfileaccesslog-properties"></a>

`Format`  <a name="cfn-appmesh-virtualgateway-virtualgatewayfileaccesslog-format"></a>
The specified format for the virtual gateway access logs\. It can be either `json_format` or `text_format`\.  
*Required*: No  
*Type*: [LoggingFormat](aws-properties-appmesh-virtualgateway-loggingformat.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-appmesh-virtualgateway-virtualgatewayfileaccesslog-path"></a>
The file path to write access logs to\. You can use `/dev/stdout` to send access logs to standard out and configure your Envoy container to use a log driver, such as `awslogs`, to export the access logs to a log storage service such as Amazon CloudWatch Logs\. You can also specify a path in the Envoy container's file system to write the files to disk\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)