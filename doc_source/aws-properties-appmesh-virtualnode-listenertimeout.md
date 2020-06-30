# AWS::AppMesh::VirtualNode ListenerTimeout<a name="aws-properties-appmesh-virtualnode-listenertimeout"></a>

An object that represents timeouts for different protocols\.

## Syntax<a name="aws-properties-appmesh-virtualnode-listenertimeout-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-listenertimeout-syntax.json"></a>

```
{
  "[GRPC](#cfn-appmesh-virtualnode-listenertimeout-grpc)" : [GrpcTimeout](aws-properties-appmesh-virtualnode-grpctimeout.md),
  "[HTTP](#cfn-appmesh-virtualnode-listenertimeout-http)" : [HttpTimeout](aws-properties-appmesh-virtualnode-httptimeout.md),
  "[HTTP2](#cfn-appmesh-virtualnode-listenertimeout-http2)" : [HttpTimeout](aws-properties-appmesh-virtualnode-httptimeout.md),
  "[TCP](#cfn-appmesh-virtualnode-listenertimeout-tcp)" : [TcpTimeout](aws-properties-appmesh-virtualnode-tcptimeout.md)
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-listenertimeout-syntax.yaml"></a>

```
  [GRPC](#cfn-appmesh-virtualnode-listenertimeout-grpc): 
    [GrpcTimeout](aws-properties-appmesh-virtualnode-grpctimeout.md)
  [HTTP](#cfn-appmesh-virtualnode-listenertimeout-http): 
    [HttpTimeout](aws-properties-appmesh-virtualnode-httptimeout.md)
  [HTTP2](#cfn-appmesh-virtualnode-listenertimeout-http2): 
    [HttpTimeout](aws-properties-appmesh-virtualnode-httptimeout.md)
  [TCP](#cfn-appmesh-virtualnode-listenertimeout-tcp): 
    [TcpTimeout](aws-properties-appmesh-virtualnode-tcptimeout.md)
```

## Properties<a name="aws-properties-appmesh-virtualnode-listenertimeout-properties"></a>

`GRPC`  <a name="cfn-appmesh-virtualnode-listenertimeout-grpc"></a>
An object that represents types of timeouts\.   
*Required*: No  
*Type*: [GrpcTimeout](aws-properties-appmesh-virtualnode-grpctimeout.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HTTP`  <a name="cfn-appmesh-virtualnode-listenertimeout-http"></a>
An object that represents types of timeouts\.   
*Required*: No  
*Type*: [HttpTimeout](aws-properties-appmesh-virtualnode-httptimeout.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HTTP2`  <a name="cfn-appmesh-virtualnode-listenertimeout-http2"></a>
An object that represents types of timeouts\.   
*Required*: No  
*Type*: [HttpTimeout](aws-properties-appmesh-virtualnode-httptimeout.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TCP`  <a name="cfn-appmesh-virtualnode-listenertimeout-tcp"></a>
An object that represents types of timeouts\.   
*Required*: No  
*Type*: [TcpTimeout](aws-properties-appmesh-virtualnode-tcptimeout.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)