# AWS::AppMesh::GatewayRoute GatewayRouteHostnameMatch<a name="aws-properties-appmesh-gatewayroute-gatewayroutehostnamematch"></a>

An object representing the gateway route host name to match\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-gatewayroutehostnamematch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-gatewayroutehostnamematch-syntax.json"></a>

```
{
  "[Exact](#cfn-appmesh-gatewayroute-gatewayroutehostnamematch-exact)" : String,
  "[Suffix](#cfn-appmesh-gatewayroute-gatewayroutehostnamematch-suffix)" : String
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-gatewayroutehostnamematch-syntax.yaml"></a>

```
  [Exact](#cfn-appmesh-gatewayroute-gatewayroutehostnamematch-exact): String
  [Suffix](#cfn-appmesh-gatewayroute-gatewayroutehostnamematch-suffix): String
```

## Properties<a name="aws-properties-appmesh-gatewayroute-gatewayroutehostnamematch-properties"></a>

`Exact`  <a name="cfn-appmesh-gatewayroute-gatewayroutehostnamematch-exact"></a>
The exact host name to match on\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `253`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Suffix`  <a name="cfn-appmesh-gatewayroute-gatewayroutehostnamematch-suffix"></a>
The specified ending characters of the host name to match on\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `253`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)