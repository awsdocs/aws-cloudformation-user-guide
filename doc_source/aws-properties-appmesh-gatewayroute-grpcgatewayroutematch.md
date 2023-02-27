# AWS::AppMesh::GatewayRoute GrpcGatewayRouteMatch<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutematch"></a>

An object that represents the criteria for determining a request match\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutematch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutematch-syntax.json"></a>

```
{
  "[Hostname](#cfn-appmesh-gatewayroute-grpcgatewayroutematch-hostname)" : GatewayRouteHostnameMatch,
  "[Metadata](#cfn-appmesh-gatewayroute-grpcgatewayroutematch-metadata)" : [ GrpcGatewayRouteMetadata, ... ],
  "[Port](#cfn-appmesh-gatewayroute-grpcgatewayroutematch-port)" : Integer,
  "[ServiceName](#cfn-appmesh-gatewayroute-grpcgatewayroutematch-servicename)" : String
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutematch-syntax.yaml"></a>

```
  [Hostname](#cfn-appmesh-gatewayroute-grpcgatewayroutematch-hostname): 
    GatewayRouteHostnameMatch
  [Metadata](#cfn-appmesh-gatewayroute-grpcgatewayroutematch-metadata): 
    - GrpcGatewayRouteMetadata
  [Port](#cfn-appmesh-gatewayroute-grpcgatewayroutematch-port): Integer
  [ServiceName](#cfn-appmesh-gatewayroute-grpcgatewayroutematch-servicename): String
```

## Properties<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutematch-properties"></a>

`Hostname`  <a name="cfn-appmesh-gatewayroute-grpcgatewayroutematch-hostname"></a>
The gateway route host name to be matched on\.  
*Required*: No  
*Type*: [GatewayRouteHostnameMatch](aws-properties-appmesh-gatewayroute-gatewayroutehostnamematch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Metadata`  <a name="cfn-appmesh-gatewayroute-grpcgatewayroutematch-metadata"></a>
The gateway route metadata to be matched on\.  
*Required*: No  
*Type*: List of [GrpcGatewayRouteMetadata](aws-properties-appmesh-gatewayroute-grpcgatewayroutemetadata.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-appmesh-gatewayroute-grpcgatewayroutematch-port"></a>
The gateway route port to be matched on\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceName`  <a name="cfn-appmesh-gatewayroute-grpcgatewayroutematch-servicename"></a>
The fully qualified domain name for the service to match from the request\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)