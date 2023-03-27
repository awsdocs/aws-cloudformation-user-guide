# AWS::NetworkManager::ConnectPeer<a name="aws-resource-networkmanager-connectpeer"></a>

Creates a core network Connect peer for a specified core network connect attachment between a core network and an appliance\. The peer address and transit gateway address must be the same IP address family \(IPv4 or IPv6\)\.

## Syntax<a name="aws-resource-networkmanager-connectpeer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkmanager-connectpeer-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkManager::ConnectPeer",
  "Properties" : {
      "[BgpOptions](#cfn-networkmanager-connectpeer-bgpoptions)" : BgpOptions,
      "[ConnectAttachmentId](#cfn-networkmanager-connectpeer-connectattachmentid)" : String,
      "[CoreNetworkAddress](#cfn-networkmanager-connectpeer-corenetworkaddress)" : String,
      "[InsideCidrBlocks](#cfn-networkmanager-connectpeer-insidecidrblocks)" : [ String, ... ],
      "[PeerAddress](#cfn-networkmanager-connectpeer-peeraddress)" : String,
      "[Tags](#cfn-networkmanager-connectpeer-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-networkmanager-connectpeer-syntax.yaml"></a>

```
Type: AWS::NetworkManager::ConnectPeer
Properties: 
  [BgpOptions](#cfn-networkmanager-connectpeer-bgpoptions): 
    BgpOptions
  [ConnectAttachmentId](#cfn-networkmanager-connectpeer-connectattachmentid): String
  [CoreNetworkAddress](#cfn-networkmanager-connectpeer-corenetworkaddress): String
  [InsideCidrBlocks](#cfn-networkmanager-connectpeer-insidecidrblocks): 
    - String
  [PeerAddress](#cfn-networkmanager-connectpeer-peeraddress): String
  [Tags](#cfn-networkmanager-connectpeer-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-networkmanager-connectpeer-properties"></a>

`BgpOptions`  <a name="cfn-networkmanager-connectpeer-bgpoptions"></a>
Property description not available\.  
*Required*: No  
*Type*: [BgpOptions](aws-properties-networkmanager-connectpeer-bgpoptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConnectAttachmentId`  <a name="cfn-networkmanager-connectpeer-connectattachmentid"></a>
The ID of the attachment to connect\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `50`  
*Pattern*: `^attachment-([0-9a-f]{8,17})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CoreNetworkAddress`  <a name="cfn-networkmanager-connectpeer-corenetworkaddress"></a>
The IP address of a core network\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Pattern*: `[\s\S]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InsideCidrBlocks`  <a name="cfn-networkmanager-connectpeer-insidecidrblocks"></a>
The inside IP addresses used for a Connect peer configuration\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PeerAddress`  <a name="cfn-networkmanager-connectpeer-peeraddress"></a>
The IP address of the Connect peer\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Pattern*: `[\s\S]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-networkmanager-connectpeer-tags"></a>
The list of key\-value tags associated with the Connect peer\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-networkmanager-connectpeer-return-values"></a>

### Ref<a name="aws-resource-networkmanager-connectpeer-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `ConnectPeerId`\. For example, `{ "Ref: "connect-peer--041e25dbc928d7e61" }`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-networkmanager-connectpeer-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-networkmanager-connectpeer-return-values-fn--getatt-fn--getatt"></a>

`Configuration`  <a name="Configuration-fn::getatt"></a>
Property description not available\.

`Configuration.BgpConfigurations`  <a name="Configuration.BgpConfigurations-fn::getatt"></a>
Property description not available\.

`Configuration.CoreNetworkAddress`  <a name="Configuration.CoreNetworkAddress-fn::getatt"></a>
Property description not available\.

`Configuration.InsideCidrBlocks`  <a name="Configuration.InsideCidrBlocks-fn::getatt"></a>
Property description not available\.

`Configuration.PeerAddress`  <a name="Configuration.PeerAddress-fn::getatt"></a>
Property description not available\.

`Configuration.Protocol`  <a name="Configuration.Protocol-fn::getatt"></a>
Property description not available\.

`ConnectPeerId`  <a name="ConnectPeerId-fn::getatt"></a>
The ID of the Connect peer\.

`CoreNetworkId`  <a name="CoreNetworkId-fn::getatt"></a>
The core network ID\.

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The timestamp when the Connect peer was created\.

`EdgeLocation`  <a name="EdgeLocation-fn::getatt"></a>
The Region where the edge is located\.

`State`  <a name="State-fn::getatt"></a>
The state of the Connect peer\. This will be: `REJECTED` \| `PENDING_ATTACHMENT_ACCEPTANCE` \| `CREATING` \| `FAILED` \| `AVAILABLE` \| `UPDATING` \| ` PENDING_NETWORK_UPDATE` \| `PENDING_TAG_ACCEPTANCE` \| `DELETING`\. 