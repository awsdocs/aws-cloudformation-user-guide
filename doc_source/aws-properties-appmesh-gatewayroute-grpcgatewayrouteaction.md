# AWS::AppMesh::GatewayRoute GrpcGatewayRouteAction<a name="aws-properties-appmesh-gatewayroute-grpcgatewayrouteaction"></a>

An object that represents the action to take if a match is determined\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-grpcgatewayrouteaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-grpcgatewayrouteaction-syntax.json"></a>

```
{
  "[Rewrite](#cfn-appmesh-gatewayroute-grpcgatewayrouteaction-rewrite)" : GrpcGatewayRouteRewrite,
  "[Target](#cfn-appmesh-gatewayroute-grpcgatewayrouteaction-target)" : GatewayRouteTarget
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-grpcgatewayrouteaction-syntax.yaml"></a>

```
  [Rewrite](#cfn-appmesh-gatewayroute-grpcgatewayrouteaction-rewrite): 
    GrpcGatewayRouteRewrite
  [Target](#cfn-appmesh-gatewayroute-grpcgatewayrouteaction-target): 
    GatewayRouteTarget
```

## Properties<a name="aws-properties-appmesh-gatewayroute-grpcgatewayrouteaction-properties"></a>

`Rewrite`  <a name="cfn-appmesh-gatewayroute-grpcgatewayrouteaction-rewrite"></a>
The gateway route action to rewrite\.  
*Required*: No  
*Type*: [GrpcGatewayRouteRewrite](aws-properties-appmesh-gatewayroute-grpcgatewayrouterewrite.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-appmesh-gatewayroute-grpcgatewayrouteaction-target"></a>
An object that represents the target that traffic is routed to when a request matches the gateway route\.  
*Required*: Yes  
*Type*: [GatewayRouteTarget](aws-properties-appmesh-gatewayroute-gatewayroutetarget.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)