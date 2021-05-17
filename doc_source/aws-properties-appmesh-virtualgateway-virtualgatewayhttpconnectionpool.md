# AWS::AppMesh::VirtualGateway VirtualGatewayHttpConnectionPool<a name="aws-properties-appmesh-virtualgateway-virtualgatewayhttpconnectionpool"></a>

An object that represents a type of connection pool\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewayhttpconnectionpool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewayhttpconnectionpool-syntax.json"></a>

```
{
  "[MaxConnections](#cfn-appmesh-virtualgateway-virtualgatewayhttpconnectionpool-maxconnections)" : Integer,
  "[MaxPendingRequests](#cfn-appmesh-virtualgateway-virtualgatewayhttpconnectionpool-maxpendingrequests)" : Integer
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewayhttpconnectionpool-syntax.yaml"></a>

```
  [MaxConnections](#cfn-appmesh-virtualgateway-virtualgatewayhttpconnectionpool-maxconnections): Integer
  [MaxPendingRequests](#cfn-appmesh-virtualgateway-virtualgatewayhttpconnectionpool-maxpendingrequests): Integer
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewayhttpconnectionpool-properties"></a>

`MaxConnections`  <a name="cfn-appmesh-virtualgateway-virtualgatewayhttpconnectionpool-maxconnections"></a>
Maximum number of outbound TCP connections Envoy can establish concurrently with all hosts in upstream cluster\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxPendingRequests`  <a name="cfn-appmesh-virtualgateway-virtualgatewayhttpconnectionpool-maxpendingrequests"></a>
Number of overflowing requests after `max_connections` Envoy will queue to upstream cluster\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)