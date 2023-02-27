# AWS::NetworkManager::SiteToSiteVpnAttachment<a name="aws-resource-networkmanager-sitetositevpnattachment"></a>

Creates an Amazon Web Services site\-to\-site VPN attachment on an edge location of a core network\.

## Syntax<a name="aws-resource-networkmanager-sitetositevpnattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkmanager-sitetositevpnattachment-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkManager::SiteToSiteVpnAttachment",
  "Properties" : {
      "[CoreNetworkId](#cfn-networkmanager-sitetositevpnattachment-corenetworkid)" : String,
      "[Tags](#cfn-networkmanager-sitetositevpnattachment-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpnConnectionArn](#cfn-networkmanager-sitetositevpnattachment-vpnconnectionarn)" : String
    }
}
```

### YAML<a name="aws-resource-networkmanager-sitetositevpnattachment-syntax.yaml"></a>

```
Type: AWS::NetworkManager::SiteToSiteVpnAttachment
Properties: 
  [CoreNetworkId](#cfn-networkmanager-sitetositevpnattachment-corenetworkid): String
  [Tags](#cfn-networkmanager-sitetositevpnattachment-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpnConnectionArn](#cfn-networkmanager-sitetositevpnattachment-vpnconnectionarn): String
```

## Properties<a name="aws-resource-networkmanager-sitetositevpnattachment-properties"></a>

`CoreNetworkId`  <a name="cfn-networkmanager-sitetositevpnattachment-corenetworkid"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-networkmanager-sitetositevpnattachment-tags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpnConnectionArn`  <a name="cfn-networkmanager-sitetositevpnattachment-vpnconnectionarn"></a>
The ARN of the site\-to\-site VPN attachment\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `500`  
*Pattern*: `^arn:[^:]{1,63}:ec2:[^:]{0,63}:[^:]{0,63}:vpn-connection\/vpn-[0-9a-f]{8,17}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-networkmanager-sitetositevpnattachment-return-values"></a>

### Ref<a name="aws-resource-networkmanager-sitetositevpnattachment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `AttachmentId`\. For example, `{ "Ref: "attachment-05467e74104d33861" }`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-networkmanager-sitetositevpnattachment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-networkmanager-sitetositevpnattachment-return-values-fn--getatt-fn--getatt"></a>

`AttachmentId`  <a name="AttachmentId-fn::getatt"></a>
The ID of the site\-to\-site VPN attachment\.

`AttachmentPolicyRuleNumber`  <a name="AttachmentPolicyRuleNumber-fn::getatt"></a>
The policy rule number associated with the attachment\.

`AttachmentType`  <a name="AttachmentType-fn::getatt"></a>
The type of attachment\. This will be `SITE_TO_SITE_VPN`\.

`CoreNetworkArn`  <a name="CoreNetworkArn-fn::getatt"></a>
The ARN of the core network\. 

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The timestamp when the site\-to\-site VPN attachment was created\.

`EdgeLocation`  <a name="EdgeLocation-fn::getatt"></a>
The Region where the core network edge is located\.

`OwnerAccountId`  <a name="OwnerAccountId-fn::getatt"></a>
The ID of the site\-to\-site VPN attachment owner\.

`ProposedSegmentChange`  <a name="ProposedSegmentChange-fn::getatt"></a>
Property description not available\.

`ProposedSegmentChange.AttachmentPolicyRuleNumber`  <a name="ProposedSegmentChange.AttachmentPolicyRuleNumber-fn::getatt"></a>
Property description not available\.

`ProposedSegmentChange.SegmentName`  <a name="ProposedSegmentChange.SegmentName-fn::getatt"></a>
Property description not available\.

`ProposedSegmentChange.Tags`  <a name="ProposedSegmentChange.Tags-fn::getatt"></a>
Property description not available\.

`ResourceArn`  <a name="ResourceArn-fn::getatt"></a>
The resource ARN for the site\-to\-site VPN attachment\.

`SegmentName`  <a name="SegmentName-fn::getatt"></a>
The name of the site\-to\-site VPN attachment's segment\.

`State`  <a name="State-fn::getatt"></a>
The state of the site\-to\-site VPN attachment\. This can be: `REJECTED` \| `PENDING_ATTACHMENT_ACCEPTANCE` \| `CREATING` \| `FAILED` \| `AVAILABLE` \| `UPDATING` \| ` PENDING_NETWORK_UPDATE` \| `PENDING_TAG_ACCEPTANCE` \| `DELETING`\. 

`UpdatedAt`  <a name="UpdatedAt-fn::getatt"></a>
The timestamp when the site\-to\-site VPN attachment was last updated\.