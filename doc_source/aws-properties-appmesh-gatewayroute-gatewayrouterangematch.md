# AWS::AppMesh::GatewayRoute GatewayRouteRangeMatch<a name="aws-properties-appmesh-gatewayroute-gatewayrouterangematch"></a>

An object that represents the range of values to match on\. The first character of the range is included in the range, though the last character is not\. For example, if the range specified were 1\-100, only values 1\-99 would be matched\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-gatewayrouterangematch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-gatewayrouterangematch-syntax.json"></a>

```
{
  "[End](#cfn-appmesh-gatewayroute-gatewayrouterangematch-end)" : Integer,
  "[Start](#cfn-appmesh-gatewayroute-gatewayrouterangematch-start)" : Integer
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-gatewayrouterangematch-syntax.yaml"></a>

```
  [End](#cfn-appmesh-gatewayroute-gatewayrouterangematch-end): Integer
  [Start](#cfn-appmesh-gatewayroute-gatewayrouterangematch-start): Integer
```

## Properties<a name="aws-properties-appmesh-gatewayroute-gatewayrouterangematch-properties"></a>

`End`  <a name="cfn-appmesh-gatewayroute-gatewayrouterangematch-end"></a>
The end of the range\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Start`  <a name="cfn-appmesh-gatewayroute-gatewayrouterangematch-start"></a>
The start of the range\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)