# AWS::AppMesh::VirtualGateway VirtualGatewayAccessLog<a name="aws-properties-appmesh-virtualgateway-virtualgatewayaccesslog"></a>

The access log configuration for a virtual gateway\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewayaccesslog-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewayaccesslog-syntax.json"></a>

```
{
  "[File](#cfn-appmesh-virtualgateway-virtualgatewayaccesslog-file)" : VirtualGatewayFileAccessLog
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewayaccesslog-syntax.yaml"></a>

```
  [File](#cfn-appmesh-virtualgateway-virtualgatewayaccesslog-file): 
    VirtualGatewayFileAccessLog
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewayaccesslog-properties"></a>

`File`  <a name="cfn-appmesh-virtualgateway-virtualgatewayaccesslog-file"></a>
The file object to send virtual gateway access logs to\.  
*Required*: No  
*Type*: [VirtualGatewayFileAccessLog](aws-properties-appmesh-virtualgateway-virtualgatewayfileaccesslog.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)