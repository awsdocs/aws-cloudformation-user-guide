# AWS::AppMesh::GatewayRoute GrpcGatewayRouteMetadata<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutemetadata"></a>

An object representing the metadata of the gateway route\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutemetadata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutemetadata-syntax.json"></a>

```
{
  "[Invert](#cfn-appmesh-gatewayroute-grpcgatewayroutemetadata-invert)" : Boolean,
  "[Match](#cfn-appmesh-gatewayroute-grpcgatewayroutemetadata-match)" : GatewayRouteMetadataMatch,
  "[Name](#cfn-appmesh-gatewayroute-grpcgatewayroutemetadata-name)" : String
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutemetadata-syntax.yaml"></a>

```
  [Invert](#cfn-appmesh-gatewayroute-grpcgatewayroutemetadata-invert): Boolean
  [Match](#cfn-appmesh-gatewayroute-grpcgatewayroutemetadata-match): 
    GatewayRouteMetadataMatch
  [Name](#cfn-appmesh-gatewayroute-grpcgatewayroutemetadata-name): String
```

## Properties<a name="aws-properties-appmesh-gatewayroute-grpcgatewayroutemetadata-properties"></a>

`Invert`  <a name="cfn-appmesh-gatewayroute-grpcgatewayroutemetadata-invert"></a>
Specify `True` to match anything except the match criteria\. The default value is `False`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Match`  <a name="cfn-appmesh-gatewayroute-grpcgatewayroutemetadata-match"></a>
The criteria for determining a metadata match\.  
*Required*: No  
*Type*: [GatewayRouteMetadataMatch](aws-properties-appmesh-gatewayroute-gatewayroutemetadatamatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appmesh-gatewayroute-grpcgatewayroutemetadata-name"></a>
A name for the gateway route metadata\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)