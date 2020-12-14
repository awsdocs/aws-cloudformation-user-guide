# AWS::AppMesh::VirtualNode HealthCheck<a name="aws-properties-appmesh-virtualnode-healthcheck"></a>

An object that represents the health check policy for a virtual node's listener\.

## Syntax<a name="aws-properties-appmesh-virtualnode-healthcheck-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-healthcheck-syntax.json"></a>

```
{
  "[HealthyThreshold](#cfn-appmesh-virtualnode-healthcheck-healthythreshold)" : Integer,
  "[IntervalMillis](#cfn-appmesh-virtualnode-healthcheck-intervalmillis)" : Integer,
  "[Path](#cfn-appmesh-virtualnode-healthcheck-path)" : String,
  "[Port](#cfn-appmesh-virtualnode-healthcheck-port)" : Integer,
  "[Protocol](#cfn-appmesh-virtualnode-healthcheck-protocol)" : String,
  "[TimeoutMillis](#cfn-appmesh-virtualnode-healthcheck-timeoutmillis)" : Integer,
  "[UnhealthyThreshold](#cfn-appmesh-virtualnode-healthcheck-unhealthythreshold)" : Integer
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-healthcheck-syntax.yaml"></a>

```
  [HealthyThreshold](#cfn-appmesh-virtualnode-healthcheck-healthythreshold): Integer
  [IntervalMillis](#cfn-appmesh-virtualnode-healthcheck-intervalmillis): Integer
  [Path](#cfn-appmesh-virtualnode-healthcheck-path): String
  [Port](#cfn-appmesh-virtualnode-healthcheck-port): Integer
  [Protocol](#cfn-appmesh-virtualnode-healthcheck-protocol): String
  [TimeoutMillis](#cfn-appmesh-virtualnode-healthcheck-timeoutmillis): Integer
  [UnhealthyThreshold](#cfn-appmesh-virtualnode-healthcheck-unhealthythreshold): Integer
```

## Properties<a name="aws-properties-appmesh-virtualnode-healthcheck-properties"></a>

`HealthyThreshold`  <a name="cfn-appmesh-virtualnode-healthcheck-healthythreshold"></a>
The number of consecutive successful health checks that must occur before declaring listener healthy\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntervalMillis`  <a name="cfn-appmesh-virtualnode-healthcheck-intervalmillis"></a>
The time period in milliseconds between each health check execution\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-appmesh-virtualnode-healthcheck-path"></a>
The destination path for the health check request\. This value is only used if the specified protocol is HTTP or HTTP/2\. For any other protocol, this value is ignored\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-appmesh-virtualnode-healthcheck-port"></a>
The destination port for the health check request\. This port must match the port defined in the [PortMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-appmesh-virtualnode-listener.html#cfn-appmesh-virtualnode-listener-portmapping) for the listener\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-appmesh-virtualnode-healthcheck-protocol"></a>
The protocol for the health check request\. If you specify `grpc`, then your service must conform to the [GRPC Health Checking Protocol](https://github.com/grpc/grpc/blob/master/doc/health-checking.md)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutMillis`  <a name="cfn-appmesh-virtualnode-healthcheck-timeoutmillis"></a>
The amount of time to wait when receiving a response from the health check, in milliseconds\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnhealthyThreshold`  <a name="cfn-appmesh-virtualnode-healthcheck-unhealthythreshold"></a>
The number of consecutive failed health checks that must occur before declaring a virtual node unhealthy\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)