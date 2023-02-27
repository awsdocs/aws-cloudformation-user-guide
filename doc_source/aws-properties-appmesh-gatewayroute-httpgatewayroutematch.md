# AWS::AppMesh::GatewayRoute HttpGatewayRouteMatch<a name="aws-properties-appmesh-gatewayroute-httpgatewayroutematch"></a>

An object that represents the criteria for determining a request match\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-httpgatewayroutematch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-httpgatewayroutematch-syntax.json"></a>

```
{
  "[Headers](#cfn-appmesh-gatewayroute-httpgatewayroutematch-headers)" : [ HttpGatewayRouteHeader, ... ],
  "[Hostname](#cfn-appmesh-gatewayroute-httpgatewayroutematch-hostname)" : GatewayRouteHostnameMatch,
  "[Method](#cfn-appmesh-gatewayroute-httpgatewayroutematch-method)" : String,
  "[Path](#cfn-appmesh-gatewayroute-httpgatewayroutematch-path)" : HttpPathMatch,
  "[Port](#cfn-appmesh-gatewayroute-httpgatewayroutematch-port)" : Integer,
  "[Prefix](#cfn-appmesh-gatewayroute-httpgatewayroutematch-prefix)" : String,
  "[QueryParameters](#cfn-appmesh-gatewayroute-httpgatewayroutematch-queryparameters)" : [ QueryParameter, ... ]
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-httpgatewayroutematch-syntax.yaml"></a>

```
  [Headers](#cfn-appmesh-gatewayroute-httpgatewayroutematch-headers): 
    - HttpGatewayRouteHeader
  [Hostname](#cfn-appmesh-gatewayroute-httpgatewayroutematch-hostname): 
    GatewayRouteHostnameMatch
  [Method](#cfn-appmesh-gatewayroute-httpgatewayroutematch-method): String
  [Path](#cfn-appmesh-gatewayroute-httpgatewayroutematch-path): 
    HttpPathMatch
  [Port](#cfn-appmesh-gatewayroute-httpgatewayroutematch-port): Integer
  [Prefix](#cfn-appmesh-gatewayroute-httpgatewayroutematch-prefix): String
  [QueryParameters](#cfn-appmesh-gatewayroute-httpgatewayroutematch-queryparameters): 
    - QueryParameter
```

## Properties<a name="aws-properties-appmesh-gatewayroute-httpgatewayroutematch-properties"></a>

`Headers`  <a name="cfn-appmesh-gatewayroute-httpgatewayroutematch-headers"></a>
The client request headers to match on\.  
*Required*: No  
*Type*: List of [HttpGatewayRouteHeader](aws-properties-appmesh-gatewayroute-httpgatewayrouteheader.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Hostname`  <a name="cfn-appmesh-gatewayroute-httpgatewayroutematch-hostname"></a>
The host name to match on\.  
*Required*: No  
*Type*: [GatewayRouteHostnameMatch](aws-properties-appmesh-gatewayroute-gatewayroutehostnamematch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Method`  <a name="cfn-appmesh-gatewayroute-httpgatewayroutematch-method"></a>
The method to match on\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CONNECT | DELETE | GET | HEAD | OPTIONS | PATCH | POST | PUT | TRACE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-appmesh-gatewayroute-httpgatewayroutematch-path"></a>
The path to match on\.  
*Required*: No  
*Type*: [HttpPathMatch](aws-properties-appmesh-gatewayroute-httppathmatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-appmesh-gatewayroute-httpgatewayroutematch-port"></a>
The port number to match on\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-appmesh-gatewayroute-httpgatewayroutematch-prefix"></a>
Specifies the path to match requests with\. This parameter must always start with `/`, which by itself matches all requests to the virtual service name\. You can also match for path\-based routing of requests\. For example, if your virtual service name is `my-service.local` and you want the route to match requests to `my-service.local/metrics`, your prefix should be `/metrics`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryParameters`  <a name="cfn-appmesh-gatewayroute-httpgatewayroutematch-queryparameters"></a>
The query parameter to match on\.  
*Required*: No  
*Type*: List of [QueryParameter](aws-properties-appmesh-gatewayroute-queryparameter.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)