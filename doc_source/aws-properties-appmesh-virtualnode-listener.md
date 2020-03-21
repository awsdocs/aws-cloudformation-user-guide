# AWS::AppMesh::VirtualNode Listener<a name="aws-properties-appmesh-virtualnode-listener"></a>

An object that represents a listener for a virtual node\.

## Syntax<a name="aws-properties-appmesh-virtualnode-listener-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-listener-syntax.json"></a>

```
{
  "[HealthCheck](#cfn-appmesh-virtualnode-listener-healthcheck)" : [HealthCheck](aws-properties-appmesh-virtualnode-healthcheck.md),
  "[PortMapping](#cfn-appmesh-virtualnode-listener-portmapping)" : [PortMapping](aws-properties-appmesh-virtualnode-portmapping.md),
  "[TLS](#cfn-appmesh-virtualnode-listener-tls)" : [ListenerTls](aws-properties-appmesh-virtualnode-listenertls.md)
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-listener-syntax.yaml"></a>

```
  [HealthCheck](#cfn-appmesh-virtualnode-listener-healthcheck): 
    [HealthCheck](aws-properties-appmesh-virtualnode-healthcheck.md)
  [PortMapping](#cfn-appmesh-virtualnode-listener-portmapping): 
    [PortMapping](aws-properties-appmesh-virtualnode-portmapping.md)
  [TLS](#cfn-appmesh-virtualnode-listener-tls): 
    [ListenerTls](aws-properties-appmesh-virtualnode-listenertls.md)
```

## Properties<a name="aws-properties-appmesh-virtualnode-listener-properties"></a>

`HealthCheck`  <a name="cfn-appmesh-virtualnode-listener-healthcheck"></a>
The health check information for the listener\.  
*Required*: No  
*Type*: [HealthCheck](aws-properties-appmesh-virtualnode-healthcheck.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortMapping`  <a name="cfn-appmesh-virtualnode-listener-portmapping"></a>
The port mapping information for the listener\.  
*Required*: Yes  
*Type*: [PortMapping](aws-properties-appmesh-virtualnode-portmapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TLS`  <a name="cfn-appmesh-virtualnode-listener-tls"></a>
A reference to an object that represents the Transport Layer Security \(TLS\) properties for a listener\.  
*Required*: No  
*Type*: [ListenerTls](aws-properties-appmesh-virtualnode-listenertls.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)