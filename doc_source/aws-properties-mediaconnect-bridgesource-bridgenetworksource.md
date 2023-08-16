# AWS::MediaConnect::BridgeSource BridgeNetworkSource<a name="aws-properties-mediaconnect-bridgesource-bridgenetworksource"></a>

The source of the bridge\. A network source originates at your premises\.

## Syntax<a name="aws-properties-mediaconnect-bridgesource-bridgenetworksource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconnect-bridgesource-bridgenetworksource-syntax.json"></a>

```
{
  "[MulticastIp](#cfn-mediaconnect-bridgesource-bridgenetworksource-multicastip)" : String,
  "[NetworkName](#cfn-mediaconnect-bridgesource-bridgenetworksource-networkname)" : String,
  "[Port](#cfn-mediaconnect-bridgesource-bridgenetworksource-port)" : Integer,
  "[Protocol](#cfn-mediaconnect-bridgesource-bridgenetworksource-protocol)" : String
}
```

### YAML<a name="aws-properties-mediaconnect-bridgesource-bridgenetworksource-syntax.yaml"></a>

```
  [MulticastIp](#cfn-mediaconnect-bridgesource-bridgenetworksource-multicastip): String
  [NetworkName](#cfn-mediaconnect-bridgesource-bridgenetworksource-networkname): String
  [Port](#cfn-mediaconnect-bridgesource-bridgenetworksource-port): Integer
  [Protocol](#cfn-mediaconnect-bridgesource-bridgenetworksource-protocol): String
```

## Properties<a name="aws-properties-mediaconnect-bridgesource-bridgenetworksource-properties"></a>

`MulticastIp`  <a name="cfn-mediaconnect-bridgesource-bridgenetworksource-multicastip"></a>
The network source multicast IP\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkName`  <a name="cfn-mediaconnect-bridgesource-bridgenetworksource-networkname"></a>
The network source's gateway network name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-mediaconnect-bridgesource-bridgenetworksource-port"></a>
The network source port\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-mediaconnect-bridgesource-bridgenetworksource-protocol"></a>
The network source protocol\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)