# AWS::AppMesh::VirtualGateway VirtualGatewayPortMapping<a name="aws-properties-appmesh-virtualgateway-virtualgatewayportmapping"></a>

An object that represents a port mapping\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewayportmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewayportmapping-syntax.json"></a>

```
{
  "[Port](#cfn-appmesh-virtualgateway-virtualgatewayportmapping-port)" : Integer,
  "[Protocol](#cfn-appmesh-virtualgateway-virtualgatewayportmapping-protocol)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewayportmapping-syntax.yaml"></a>

```
  [Port](#cfn-appmesh-virtualgateway-virtualgatewayportmapping-port): Integer
  [Protocol](#cfn-appmesh-virtualgateway-virtualgatewayportmapping-protocol): String
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewayportmapping-properties"></a>

`Port`  <a name="cfn-appmesh-virtualgateway-virtualgatewayportmapping-port"></a>
The port used for the port mapping\. Specify one protocol\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-appmesh-virtualgateway-virtualgatewayportmapping-protocol"></a>
The protocol used for the port mapping\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)