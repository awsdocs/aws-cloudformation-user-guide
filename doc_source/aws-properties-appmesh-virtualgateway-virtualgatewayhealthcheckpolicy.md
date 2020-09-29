# AWS::AppMesh::VirtualGateway VirtualGatewayHealthCheckPolicy<a name="aws-properties-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy"></a>

An object that represents the health check policy for a virtual gateway's listener\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-syntax.json"></a>

```
{
  "[HealthyThreshold](#cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-healthythreshold)" : Integer,
  "[IntervalMillis](#cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-intervalmillis)" : Integer,
  "[Path](#cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-path)" : String,
  "[Port](#cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-port)" : Integer,
  "[Protocol](#cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-protocol)" : String,
  "[TimeoutMillis](#cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-timeoutmillis)" : Integer,
  "[UnhealthyThreshold](#cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-unhealthythreshold)" : Integer
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-syntax.yaml"></a>

```
  [HealthyThreshold](#cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-healthythreshold): Integer
  [IntervalMillis](#cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-intervalmillis): Integer
  [Path](#cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-path): String
  [Port](#cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-port): Integer
  [Protocol](#cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-protocol): String
  [TimeoutMillis](#cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-timeoutmillis): Integer
  [UnhealthyThreshold](#cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-unhealthythreshold): Integer
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-properties"></a>

`HealthyThreshold`  <a name="cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-healthythreshold"></a>
The number of consecutive successful health checks that must occur before declaring the listener healthy\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntervalMillis`  <a name="cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-intervalmillis"></a>
The time period in milliseconds between each health check execution\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-path"></a>
The destination path for the health check request\. This value is only used if the specified protocol is HTTP or HTTP/2\. For any other protocol, this value is ignored\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-port"></a>
The destination port for the health check request\. This port must match the port defined in the [PortMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-appmesh-virtualnode-listener.html#cfn-appmesh-virtualnode-listener-portmapping) for the listener\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-protocol"></a>
The protocol for the health check request\. If you specify `grpc`, then your service must conform to the [GRPC Health Checking Protocol](https://github.com/grpc/grpc/blob/master/doc/health-checking.md)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutMillis`  <a name="cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-timeoutmillis"></a>
The amount of time to wait when receiving a response from the health check, in milliseconds\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnhealthyThreshold`  <a name="cfn-appmesh-virtualgateway-virtualgatewayhealthcheckpolicy-unhealthythreshold"></a>
The number of consecutive failed health checks that must occur before declaring a virtual gateway unhealthy\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)