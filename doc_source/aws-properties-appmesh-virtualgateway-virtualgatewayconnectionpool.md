# AWS::AppMesh::VirtualGateway VirtualGatewayConnectionPool<a name="aws-properties-appmesh-virtualgateway-virtualgatewayconnectionpool"></a>

An object that represents the type of virtual gateway connection pool\.

Only one protocol is used at a time and should be the same protocol as the one chosen under port mapping\.

If not present the default value for `maxPendingRequests` is `2147483647`\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewayconnectionpool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewayconnectionpool-syntax.json"></a>

```
{
  "[GRPC](#cfn-appmesh-virtualgateway-virtualgatewayconnectionpool-grpc)" : VirtualGatewayGrpcConnectionPool,
  "[HTTP](#cfn-appmesh-virtualgateway-virtualgatewayconnectionpool-http)" : VirtualGatewayHttpConnectionPool,
  "[HTTP2](#cfn-appmesh-virtualgateway-virtualgatewayconnectionpool-http2)" : VirtualGatewayHttp2ConnectionPool
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewayconnectionpool-syntax.yaml"></a>

```
  [GRPC](#cfn-appmesh-virtualgateway-virtualgatewayconnectionpool-grpc): 
    VirtualGatewayGrpcConnectionPool
  [HTTP](#cfn-appmesh-virtualgateway-virtualgatewayconnectionpool-http): 
    VirtualGatewayHttpConnectionPool
  [HTTP2](#cfn-appmesh-virtualgateway-virtualgatewayconnectionpool-http2): 
    VirtualGatewayHttp2ConnectionPool
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewayconnectionpool-properties"></a>

`GRPC`  <a name="cfn-appmesh-virtualgateway-virtualgatewayconnectionpool-grpc"></a>
An object that represents a type of connection pool\.   
*Required*: No  
*Type*: [VirtualGatewayGrpcConnectionPool](aws-properties-appmesh-virtualgateway-virtualgatewaygrpcconnectionpool.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HTTP`  <a name="cfn-appmesh-virtualgateway-virtualgatewayconnectionpool-http"></a>
An object that represents a type of connection pool\.  
*Required*: No  
*Type*: [VirtualGatewayHttpConnectionPool](aws-properties-appmesh-virtualgateway-virtualgatewayhttpconnectionpool.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HTTP2`  <a name="cfn-appmesh-virtualgateway-virtualgatewayconnectionpool-http2"></a>
An object that represents a type of connection pool\.  
*Required*: No  
*Type*: [VirtualGatewayHttp2ConnectionPool](aws-properties-appmesh-virtualgateway-virtualgatewayhttp2connectionpool.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)