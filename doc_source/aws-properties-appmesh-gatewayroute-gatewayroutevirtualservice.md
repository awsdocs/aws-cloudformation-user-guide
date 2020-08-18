# AWS::AppMesh::GatewayRoute GatewayRouteVirtualService<a name="aws-properties-appmesh-gatewayroute-gatewayroutevirtualservice"></a>

An object that represents the virtual service that traffic is routed to\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-gatewayroutevirtualservice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-gatewayroutevirtualservice-syntax.json"></a>

```
{
  "[VirtualServiceName](#cfn-appmesh-gatewayroute-gatewayroutevirtualservice-virtualservicename)" : String
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-gatewayroutevirtualservice-syntax.yaml"></a>

```
  [VirtualServiceName](#cfn-appmesh-gatewayroute-gatewayroutevirtualservice-virtualservicename): String
```

## Properties<a name="aws-properties-appmesh-gatewayroute-gatewayroutevirtualservice-properties"></a>

`VirtualServiceName`  <a name="cfn-appmesh-gatewayroute-gatewayroutevirtualservice-virtualservicename"></a>
The name of the virtual service that traffic is routed to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)