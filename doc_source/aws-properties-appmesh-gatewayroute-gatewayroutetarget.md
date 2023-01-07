# AWS::AppMesh::GatewayRoute GatewayRouteTarget<a name="aws-properties-appmesh-gatewayroute-gatewayroutetarget"></a>

An object that represents a gateway route target\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-gatewayroutetarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-gatewayroutetarget-syntax.json"></a>

```
{
  "[VirtualService](#cfn-appmesh-gatewayroute-gatewayroutetarget-virtualservice)" : GatewayRouteVirtualService
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-gatewayroutetarget-syntax.yaml"></a>

```
  [VirtualService](#cfn-appmesh-gatewayroute-gatewayroutetarget-virtualservice): 
    GatewayRouteVirtualService
```

## Properties<a name="aws-properties-appmesh-gatewayroute-gatewayroutetarget-properties"></a>

`VirtualService`  <a name="cfn-appmesh-gatewayroute-gatewayroutetarget-virtualservice"></a>
An object that represents a virtual service gateway route target\.  
*Required*: Yes  
*Type*: [GatewayRouteVirtualService](aws-properties-appmesh-gatewayroute-gatewayroutevirtualservice.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)