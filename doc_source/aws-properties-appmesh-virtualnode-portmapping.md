# AWS::AppMesh::VirtualNode PortMapping<a name="aws-properties-appmesh-virtualnode-portmapping"></a>

An object representing a virtual node or virtual router listener port mapping\.

## Syntax<a name="aws-properties-appmesh-virtualnode-portmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-portmapping-syntax.json"></a>

```
{
  "[Port](#cfn-appmesh-virtualnode-portmapping-port)" : Integer,
  "[Protocol](#cfn-appmesh-virtualnode-portmapping-protocol)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-portmapping-syntax.yaml"></a>

```
  [Port](#cfn-appmesh-virtualnode-portmapping-port): Integer
  [Protocol](#cfn-appmesh-virtualnode-portmapping-protocol): String
```

## Properties<a name="aws-properties-appmesh-virtualnode-portmapping-properties"></a>

`Port`  <a name="cfn-appmesh-virtualnode-portmapping-port"></a>
The port used for the port mapping\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-appmesh-virtualnode-portmapping-protocol"></a>
The protocol used for the port mapping\. Specify `http`, `http2`, `grpc`, or `tcp`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)