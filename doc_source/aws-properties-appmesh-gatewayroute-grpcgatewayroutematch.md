# AWS::AppMesh::GatewayRoute GrpcGatewayRouteMatch<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutematch"></a>

An object that represents the criteria for determining a request match\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutematch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutematch-syntax.json"></a>

```
{
  "[ServiceName](#cfn-appmesh-gatewayroute-grpcgatewayroutematch-servicename)" : String
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutematch-syntax.yaml"></a>

```
  [ServiceName](#cfn-appmesh-gatewayroute-grpcgatewayroutematch-servicename): String
```

## Properties<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutematch-properties"></a>

`ServiceName`  <a name="cfn-appmesh-gatewayroute-grpcgatewayroutematch-servicename"></a>
The fully qualified domain name for the service to match from the request\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)