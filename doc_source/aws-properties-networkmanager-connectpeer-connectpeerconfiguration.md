# AWS::NetworkManager::ConnectPeer ConnectPeerConfiguration<a name="aws-properties-networkmanager-connectpeer-connectpeerconfiguration"></a>

Describes a core network Connect peer configuration\.

## Syntax<a name="aws-properties-networkmanager-connectpeer-connectpeerconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkmanager-connectpeer-connectpeerconfiguration-syntax.json"></a>

```
{
  "[BgpConfigurations](#cfn-networkmanager-connectpeer-connectpeerconfiguration-bgpconfigurations)" : [ ConnectPeerBgpConfiguration, ... ],
  "[CoreNetworkAddress](#cfn-networkmanager-connectpeer-connectpeerconfiguration-corenetworkaddress)" : String,
  "[InsideCidrBlocks](#cfn-networkmanager-connectpeer-connectpeerconfiguration-insidecidrblocks)" : [ String, ... ],
  "[PeerAddress](#cfn-networkmanager-connectpeer-connectpeerconfiguration-peeraddress)" : String,
  "[Protocol](#cfn-networkmanager-connectpeer-connectpeerconfiguration-protocol)" : String
}
```

### YAML<a name="aws-properties-networkmanager-connectpeer-connectpeerconfiguration-syntax.yaml"></a>

```
  [BgpConfigurations](#cfn-networkmanager-connectpeer-connectpeerconfiguration-bgpconfigurations): 
    - ConnectPeerBgpConfiguration
  [CoreNetworkAddress](#cfn-networkmanager-connectpeer-connectpeerconfiguration-corenetworkaddress): String
  [InsideCidrBlocks](#cfn-networkmanager-connectpeer-connectpeerconfiguration-insidecidrblocks): 
    - String
  [PeerAddress](#cfn-networkmanager-connectpeer-connectpeerconfiguration-peeraddress): String
  [Protocol](#cfn-networkmanager-connectpeer-connectpeerconfiguration-protocol): String
```

## Properties<a name="aws-properties-networkmanager-connectpeer-connectpeerconfiguration-properties"></a>

`BgpConfigurations`  <a name="cfn-networkmanager-connectpeer-connectpeerconfiguration-bgpconfigurations"></a>
The Connect peer BGP configurations\.  
*Required*: No  
*Type*: List of [ConnectPeerBgpConfiguration](aws-properties-networkmanager-connectpeer-connectpeerbgpconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CoreNetworkAddress`  <a name="cfn-networkmanager-connectpeer-connectpeerconfiguration-corenetworkaddress"></a>
The IP address of a core network\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Pattern*: `[\s\S]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InsideCidrBlocks`  <a name="cfn-networkmanager-connectpeer-connectpeerconfiguration-insidecidrblocks"></a>
The inside IP addresses used for a Connect peer configuration\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PeerAddress`  <a name="cfn-networkmanager-connectpeer-connectpeerconfiguration-peeraddress"></a>
The IP address of the Connect peer\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Pattern*: `[\s\S]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-networkmanager-connectpeer-connectpeerconfiguration-protocol"></a>
The protocol used for a Connect peer configuration\.  
*Required*: No  
*Type*: String  
*Allowed values*: `GRE | NO_ENCAP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)