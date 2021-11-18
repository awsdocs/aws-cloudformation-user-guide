# AWS::AppMesh::GatewayRoute HttpGatewayRouteHeader<a name="aws-properties-appmesh-gatewayroute-httpgatewayrouteheader"></a>

An object that represents the HTTP header in the gateway route\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-httpgatewayrouteheader-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-httpgatewayrouteheader-syntax.json"></a>

```
{
  "[Invert](#cfn-appmesh-gatewayroute-httpgatewayrouteheader-invert)" : Boolean,
  "[Match](#cfn-appmesh-gatewayroute-httpgatewayrouteheader-match)" : HttpGatewayRouteHeaderMatch,
  "[Name](#cfn-appmesh-gatewayroute-httpgatewayrouteheader-name)" : String
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-httpgatewayrouteheader-syntax.yaml"></a>

```
  [Invert](#cfn-appmesh-gatewayroute-httpgatewayrouteheader-invert): Boolean
  [Match](#cfn-appmesh-gatewayroute-httpgatewayrouteheader-match): 
    HttpGatewayRouteHeaderMatch
  [Name](#cfn-appmesh-gatewayroute-httpgatewayrouteheader-name): String
```

## Properties<a name="aws-properties-appmesh-gatewayroute-httpgatewayrouteheader-properties"></a>

`Invert`  <a name="cfn-appmesh-gatewayroute-httpgatewayrouteheader-invert"></a>
Specify `True` to match anything except the match criteria\. The default value is `False`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Match`  <a name="cfn-appmesh-gatewayroute-httpgatewayrouteheader-match"></a>
An object that represents the method and value to match with the header value sent in a request\. Specify one match method\.  
*Required*: No  
*Type*: [HttpGatewayRouteHeaderMatch](aws-properties-appmesh-gatewayroute-httpgatewayrouteheadermatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appmesh-gatewayroute-httpgatewayrouteheader-name"></a>
A name for the HTTP header in the gateway route that will be matched on\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)