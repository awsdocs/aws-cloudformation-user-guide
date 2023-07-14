# AWS::MediaConnect::Bridge BridgeNetworkSource<a name="aws-properties-mediaconnect-bridge-bridgenetworksource"></a>

The source of the bridge\. A network source originates at your premises\.

## Syntax<a name="aws-properties-mediaconnect-bridge-bridgenetworksource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconnect-bridge-bridgenetworksource-syntax.json"></a>

```
{
  "[MulticastIp](#cfn-mediaconnect-bridge-bridgenetworksource-multicastip)" : String,
  "[Name](#cfn-mediaconnect-bridge-bridgenetworksource-name)" : String,
  "[NetworkName](#cfn-mediaconnect-bridge-bridgenetworksource-networkname)" : String,
  "[Port](#cfn-mediaconnect-bridge-bridgenetworksource-port)" : Integer,
  "[Protocol](#cfn-mediaconnect-bridge-bridgenetworksource-protocol)" : String
}
```

### YAML<a name="aws-properties-mediaconnect-bridge-bridgenetworksource-syntax.yaml"></a>

```
  [MulticastIp](#cfn-mediaconnect-bridge-bridgenetworksource-multicastip): String
  [Name](#cfn-mediaconnect-bridge-bridgenetworksource-name): String
  [NetworkName](#cfn-mediaconnect-bridge-bridgenetworksource-networkname): String
  [Port](#cfn-mediaconnect-bridge-bridgenetworksource-port): Integer
  [Protocol](#cfn-mediaconnect-bridge-bridgenetworksource-protocol): String
```

## Properties<a name="aws-properties-mediaconnect-bridge-bridgenetworksource-properties"></a>

`MulticastIp`  <a name="cfn-mediaconnect-bridge-bridgenetworksource-multicastip"></a>
The network source multicast IP\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-mediaconnect-bridge-bridgenetworksource-name"></a>
The name of the network source\. This name is used to reference the source and must be unique among sources in this bridge\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkName`  <a name="cfn-mediaconnect-bridge-bridgenetworksource-networkname"></a>
The network source's gateway network name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-mediaconnect-bridge-bridgenetworksource-port"></a>
The network source port\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-mediaconnect-bridge-bridgenetworksource-protocol"></a>
The network source protocol\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)