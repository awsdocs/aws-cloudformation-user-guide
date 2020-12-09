# AWS::AppMesh::GatewayRoute GatewayRouteSpec<a name="aws-properties-appmesh-gatewayroute-gatewayroutespec"></a>

An object that represents a gateway route specification\. Specify one gateway route type\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-gatewayroutespec-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-gatewayroutespec-syntax.json"></a>

```
{
  "[GrpcRoute](#cfn-appmesh-gatewayroute-gatewayroutespec-grpcroute)" : GrpcGatewayRoute,
  "[Http2Route](#cfn-appmesh-gatewayroute-gatewayroutespec-http2route)" : HttpGatewayRoute,
  "[HttpRoute](#cfn-appmesh-gatewayroute-gatewayroutespec-httproute)" : HttpGatewayRoute
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-gatewayroutespec-syntax.yaml"></a>

```
  [GrpcRoute](#cfn-appmesh-gatewayroute-gatewayroutespec-grpcroute): 
    GrpcGatewayRoute
  [Http2Route](#cfn-appmesh-gatewayroute-gatewayroutespec-http2route): 
    HttpGatewayRoute
  [HttpRoute](#cfn-appmesh-gatewayroute-gatewayroutespec-httproute): 
    HttpGatewayRoute
```

## Properties<a name="aws-properties-appmesh-gatewayroute-gatewayroutespec-properties"></a>

`GrpcRoute`  <a name="cfn-appmesh-gatewayroute-gatewayroutespec-grpcroute"></a>
An object that represents the specification of a gRPC gateway route\.  
*Required*: No  
*Type*: [GrpcGatewayRoute](aws-properties-appmesh-gatewayroute-grpcgatewayroute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Http2Route`  <a name="cfn-appmesh-gatewayroute-gatewayroutespec-http2route"></a>
An object that represents the specification of an HTTP/2 gateway route\.  
*Required*: No  
*Type*: [HttpGatewayRoute](aws-properties-appmesh-gatewayroute-httpgatewayroute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpRoute`  <a name="cfn-appmesh-gatewayroute-gatewayroutespec-httproute"></a>
An object that represents the specification of an HTTP gateway route\.  
*Required*: No  
*Type*: [HttpGatewayRoute](aws-properties-appmesh-gatewayroute-httpgatewayroute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)