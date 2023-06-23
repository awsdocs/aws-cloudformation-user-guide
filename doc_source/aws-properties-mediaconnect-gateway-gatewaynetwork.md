# AWS::MediaConnect::Gateway GatewayNetwork<a name="aws-properties-mediaconnect-gateway-gatewaynetwork"></a>

The network settings for a gateway\.

## Syntax<a name="aws-properties-mediaconnect-gateway-gatewaynetwork-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconnect-gateway-gatewaynetwork-syntax.json"></a>

```
{
  "[CidrBlock](#cfn-mediaconnect-gateway-gatewaynetwork-cidrblock)" : String,
  "[Name](#cfn-mediaconnect-gateway-gatewaynetwork-name)" : String
}
```

### YAML<a name="aws-properties-mediaconnect-gateway-gatewaynetwork-syntax.yaml"></a>

```
  [CidrBlock](#cfn-mediaconnect-gateway-gatewaynetwork-cidrblock): String
  [Name](#cfn-mediaconnect-gateway-gatewaynetwork-name): String
```

## Properties<a name="aws-properties-mediaconnect-gateway-gatewaynetwork-properties"></a>

`CidrBlock`  <a name="cfn-mediaconnect-gateway-gatewaynetwork-cidrblock"></a>
A unique IP address range to use for this network\. These IP addresses should be in the form of a Classless Inter\-Domain Routing \(CIDR\) block; for example, 10\.0\.0\.0/16\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-mediaconnect-gateway-gatewaynetwork-name"></a>
The name of the network\. This name is used to reference the network and must be unique among networks in this gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)