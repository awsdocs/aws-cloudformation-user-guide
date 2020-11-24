# AWS::AppMesh::VirtualGateway VirtualGatewayGrpcConnectionPool<a name="aws-properties-appmesh-virtualgateway-virtualgatewaygrpcconnectionpool"></a>

An object that represents a type of connection pool\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewaygrpcconnectionpool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewaygrpcconnectionpool-syntax.json"></a>

```
{
  "[MaxRequests](#cfn-appmesh-virtualgateway-virtualgatewaygrpcconnectionpool-maxrequests)" : Integer
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewaygrpcconnectionpool-syntax.yaml"></a>

```
  [MaxRequests](#cfn-appmesh-virtualgateway-virtualgatewaygrpcconnectionpool-maxrequests): Integer
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewaygrpcconnectionpool-properties"></a>

`MaxRequests`  <a name="cfn-appmesh-virtualgateway-virtualgatewaygrpcconnectionpool-maxrequests"></a>
Maximum number of inflight requests Envoy can concurrently support across hosts in upstream cluster\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)