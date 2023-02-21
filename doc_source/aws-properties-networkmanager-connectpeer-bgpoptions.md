# AWS::NetworkManager::ConnectPeer BgpOptions<a name="aws-properties-networkmanager-connectpeer-bgpoptions"></a>

Describes the BGP options\.

## Syntax<a name="aws-properties-networkmanager-connectpeer-bgpoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkmanager-connectpeer-bgpoptions-syntax.json"></a>

```
{
  "[PeerAsn](#cfn-networkmanager-connectpeer-bgpoptions-peerasn)" : Double
}
```

### YAML<a name="aws-properties-networkmanager-connectpeer-bgpoptions-syntax.yaml"></a>

```
  [PeerAsn](#cfn-networkmanager-connectpeer-bgpoptions-peerasn): Double
```

## Properties<a name="aws-properties-networkmanager-connectpeer-bgpoptions-properties"></a>

`PeerAsn`  <a name="cfn-networkmanager-connectpeer-bgpoptions-peerasn"></a>
The Peer ASN of the BGP\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)