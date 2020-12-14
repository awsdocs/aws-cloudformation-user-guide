# AWS::AppMesh::GatewayRoute HttpGatewayRoute<a name="aws-properties-appmesh-gatewayroute-httpgatewayroute"></a>

An object that represents an HTTP gateway route\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-httpgatewayroute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-httpgatewayroute-syntax.json"></a>

```
{
  "[Action](#cfn-appmesh-gatewayroute-httpgatewayroute-action)" : HttpGatewayRouteAction,
  "[Match](#cfn-appmesh-gatewayroute-httpgatewayroute-match)" : HttpGatewayRouteMatch
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-httpgatewayroute-syntax.yaml"></a>

```
  [Action](#cfn-appmesh-gatewayroute-httpgatewayroute-action): 
    HttpGatewayRouteAction
  [Match](#cfn-appmesh-gatewayroute-httpgatewayroute-match): 
    HttpGatewayRouteMatch
```

## Properties<a name="aws-properties-appmesh-gatewayroute-httpgatewayroute-properties"></a>

`Action`  <a name="cfn-appmesh-gatewayroute-httpgatewayroute-action"></a>
An object that represents the action to take if a match is determined\.  
*Required*: Yes  
*Type*: [HttpGatewayRouteAction](aws-properties-appmesh-gatewayroute-httpgatewayrouteaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Match`  <a name="cfn-appmesh-gatewayroute-httpgatewayroute-match"></a>
An object that represents the criteria for determining a request match\.  
*Required*: Yes  
*Type*: [HttpGatewayRouteMatch](aws-properties-appmesh-gatewayroute-httpgatewayroutematch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)