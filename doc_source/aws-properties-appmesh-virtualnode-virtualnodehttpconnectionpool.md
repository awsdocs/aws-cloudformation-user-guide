# AWS::AppMesh::VirtualNode VirtualNodeHttpConnectionPool<a name="aws-properties-appmesh-virtualnode-virtualnodehttpconnectionpool"></a>

An object that represents a type of connection pool\.

## Syntax<a name="aws-properties-appmesh-virtualnode-virtualnodehttpconnectionpool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-virtualnodehttpconnectionpool-syntax.json"></a>

```
{
  "[MaxConnections](#cfn-appmesh-virtualnode-virtualnodehttpconnectionpool-maxconnections)" : Integer,
  "[MaxPendingRequests](#cfn-appmesh-virtualnode-virtualnodehttpconnectionpool-maxpendingrequests)" : Integer
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-virtualnodehttpconnectionpool-syntax.yaml"></a>

```
  [MaxConnections](#cfn-appmesh-virtualnode-virtualnodehttpconnectionpool-maxconnections): Integer
  [MaxPendingRequests](#cfn-appmesh-virtualnode-virtualnodehttpconnectionpool-maxpendingrequests): Integer
```

## Properties<a name="aws-properties-appmesh-virtualnode-virtualnodehttpconnectionpool-properties"></a>

`MaxConnections`  <a name="cfn-appmesh-virtualnode-virtualnodehttpconnectionpool-maxconnections"></a>
Maximum number of outbound TCP connections Envoy can establish concurrently with all hosts in upstream cluster\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxPendingRequests`  <a name="cfn-appmesh-virtualnode-virtualnodehttpconnectionpool-maxpendingrequests"></a>
Number of overflowing requests after `max_connections` Envoy will queue to upstream cluster\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)