# AWS::AppMesh::VirtualNode VirtualNodeHttp2ConnectionPool<a name="aws-properties-appmesh-virtualnode-virtualnodehttp2connectionpool"></a>

An object that represents a type of connection pool\.

## Syntax<a name="aws-properties-appmesh-virtualnode-virtualnodehttp2connectionpool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-virtualnodehttp2connectionpool-syntax.json"></a>

```
{
  "[MaxRequests](#cfn-appmesh-virtualnode-virtualnodehttp2connectionpool-maxrequests)" : Integer
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-virtualnodehttp2connectionpool-syntax.yaml"></a>

```
  [MaxRequests](#cfn-appmesh-virtualnode-virtualnodehttp2connectionpool-maxrequests): Integer
```

## Properties<a name="aws-properties-appmesh-virtualnode-virtualnodehttp2connectionpool-properties"></a>

`MaxRequests`  <a name="cfn-appmesh-virtualnode-virtualnodehttp2connectionpool-maxrequests"></a>
Maximum number of inflight requests Envoy can concurrently support across hosts in upstream cluster\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)