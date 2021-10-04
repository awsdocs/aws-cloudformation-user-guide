# AWS::AppMesh::GatewayRoute GrpcGatewayRouteRewrite<a name="aws-properties-appmesh-gatewayroute-grpcgatewayrouterewrite"></a>

An object that represents the gateway route to rewrite\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-grpcgatewayrouterewrite-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-grpcgatewayrouterewrite-syntax.json"></a>

```
{
  "[Hostname](#cfn-appmesh-gatewayroute-grpcgatewayrouterewrite-hostname)" : GatewayRouteHostnameRewrite
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-grpcgatewayrouterewrite-syntax.yaml"></a>

```
  [Hostname](#cfn-appmesh-gatewayroute-grpcgatewayrouterewrite-hostname): 
    GatewayRouteHostnameRewrite
```

## Properties<a name="aws-properties-appmesh-gatewayroute-grpcgatewayrouterewrite-properties"></a>

`Hostname`  <a name="cfn-appmesh-gatewayroute-grpcgatewayrouterewrite-hostname"></a>
The host name of the gateway route to rewrite\.  
*Required*: No  
*Type*: [GatewayRouteHostnameRewrite](aws-properties-appmesh-gatewayroute-gatewayroutehostnamerewrite.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)