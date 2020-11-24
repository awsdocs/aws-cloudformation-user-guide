# AWS::AppMesh::VirtualNode VirtualNodeTcpConnectionPool<a name="aws-properties-appmesh-virtualnode-virtualnodetcpconnectionpool"></a>

An object that represents a type of connection pool\.

## Syntax<a name="aws-properties-appmesh-virtualnode-virtualnodetcpconnectionpool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-virtualnodetcpconnectionpool-syntax.json"></a>

```
{
  "[MaxConnections](#cfn-appmesh-virtualnode-virtualnodetcpconnectionpool-maxconnections)" : Integer
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-virtualnodetcpconnectionpool-syntax.yaml"></a>

```
  [MaxConnections](#cfn-appmesh-virtualnode-virtualnodetcpconnectionpool-maxconnections): Integer
```

## Properties<a name="aws-properties-appmesh-virtualnode-virtualnodetcpconnectionpool-properties"></a>

`MaxConnections`  <a name="cfn-appmesh-virtualnode-virtualnodetcpconnectionpool-maxconnections"></a>
Maximum number of outbound TCP connections Envoy can establish concurrently with all hosts in upstream cluster\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)