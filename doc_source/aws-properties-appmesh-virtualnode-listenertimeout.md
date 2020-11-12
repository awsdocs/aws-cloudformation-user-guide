# AWS::AppMesh::VirtualNode ListenerTimeout<a name="aws-properties-appmesh-virtualnode-listenertimeout"></a>

An object that represents timeouts for different protocols\.

## Syntax<a name="aws-properties-appmesh-virtualnode-listenertimeout-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-listenertimeout-syntax.json"></a>

```
{
  "[GRPC](#cfn-appmesh-virtualnode-listenertimeout-grpc)" : GrpcTimeout,
  "[HTTP](#cfn-appmesh-virtualnode-listenertimeout-http)" : HttpTimeout,
  "[HTTP2](#cfn-appmesh-virtualnode-listenertimeout-http2)" : HttpTimeout,
  "[TCP](#cfn-appmesh-virtualnode-listenertimeout-tcp)" : TcpTimeout
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-listenertimeout-syntax.yaml"></a>

```
  [GRPC](#cfn-appmesh-virtualnode-listenertimeout-grpc): 
    GrpcTimeout
  [HTTP](#cfn-appmesh-virtualnode-listenertimeout-http): 
    HttpTimeout
  [HTTP2](#cfn-appmesh-virtualnode-listenertimeout-http2): 
    HttpTimeout
  [TCP](#cfn-appmesh-virtualnode-listenertimeout-tcp): 
    TcpTimeout
```

## Properties<a name="aws-properties-appmesh-virtualnode-listenertimeout-properties"></a>

`GRPC`  <a name="cfn-appmesh-virtualnode-listenertimeout-grpc"></a>
Not currently supported by AWS CloudFormation\.  
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