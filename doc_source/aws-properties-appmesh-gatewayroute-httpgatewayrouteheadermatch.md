# AWS::AppMesh::GatewayRoute HttpGatewayRouteHeaderMatch<a name="aws-properties-appmesh-gatewayroute-httpgatewayrouteheadermatch"></a>

An object that represents the method and value to match with the header value sent in a request\. Specify one match method\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-httpgatewayrouteheadermatch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-httpgatewayrouteheadermatch-syntax.json"></a>

```
{
  "[Exact](#cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-exact)" : String,
  "[Prefix](#cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-prefix)" : String,
  "[Range](#cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-range)" : GatewayRouteRangeMatch,
  "[Regex](#cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-regex)" : String,
  "[Suffix](#cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-suffix)" : String
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-httpgatewayrouteheadermatch-syntax.yaml"></a>

```
  [Exact](#cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-exact): String
  [Prefix](#cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-prefix): String
  [Range](#cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-range): 
    GatewayRouteRangeMatch
  [Regex](#cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-regex): String
  [Suffix](#cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-suffix): String
```

## Properties<a name="aws-properties-appmesh-gatewayroute-httpgatewayrouteheadermatch-properties"></a>

`Exact`  <a name="cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-exact"></a>
The value sent by the client must match the specified value exactly\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-prefix"></a>
The value sent by the client must begin with the specified characters\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Range`  <a name="cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-range"></a>
An object that represents the range of values to match on\.  
*Required*: No  
*Type*: [GatewayRouteRangeMatch](aws-properties-appmesh-gatewayroute-gatewayrouterangematch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Regex`  <a name="cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-regex"></a>
The value sent by the client must include the specified characters\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Suffix`  <a name="cfn-appmesh-gatewayroute-httpgatewayrouteheadermatch-suffix"></a>
The value sent by the client must end with the specified characters\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)