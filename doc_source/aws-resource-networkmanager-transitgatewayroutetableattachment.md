# AWS::NetworkManager::TransitGatewayRouteTableAttachment<a name="aws-resource-networkmanager-transitgatewayroutetableattachment"></a>

Creates a transit gateway route table attachment\.

## Syntax<a name="aws-resource-networkmanager-transitgatewayroutetableattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkmanager-transitgatewayroutetableattachment-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkManager::TransitGatewayRouteTableAttachment",
  "Properties" : {
      "[PeeringId](#cfn-networkmanager-transitgatewayroutetableattachment-peeringid)" : String,
      "[ProposedSegmentChange](#cfn-networkmanager-transitgatewayroutetableattachment-proposedsegmentchange)" : ProposedSegmentChange,
      "[Tags](#cfn-networkmanager-transitgatewayroutetableattachment-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TransitGatewayRouteTableArn](#cfn-networkmanager-transitgatewayroutetableattachment-transitgatewayroutetablearn)" : String
    }
}
```

### YAML<a name="aws-resource-networkmanager-transitgatewayroutetableattachment-syntax.yaml"></a>

```
Type: AWS::NetworkManager::TransitGatewayRouteTableAttachment
Properties: 
  [PeeringId](#cfn-networkmanager-transitgatewayroutetableattachment-peeringid): String
  [ProposedSegmentChange](#cfn-networkmanager-transitgatewayroutetableattachment-proposedsegmentchange): 
    ProposedSegmentChange
  [Tags](#cfn-networkmanager-transitgatewayroutetableattachment-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TransitGatewayRouteTableArn](#cfn-networkmanager-transitgatewayroutetableattachment-transitgatewayroutetablearn): String
```

## Properties<a name="aws-resource-networkmanager-transitgatewayroutetableattachment-properties"></a>

`PeeringId`  <a name="cfn-networkmanager-transitgatewayroutetableattachment-peeringid"></a>
The ID of the transit gateway peering\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `50`  
*Pattern*: `^peering-([0-9a-f]{8,17})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProposedSegmentChange`  <a name="cfn-networkmanager-transitgatewayroutetableattachment-proposedsegmentchange"></a>
This property is read\-only\. Values can't be assigned to it\.  
*Required*: No  
*Type*: [ProposedSegmentChange](aws-properties-networkmanager-transitgatewayroutetableattachment-proposedsegmentchange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-networkmanager-transitgatewayroutetableattachment-tags"></a>
The list of key\-value pairs associated with the transit gateway route table attachment\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitGatewayRouteTableArn`  <a name="cfn-networkmanager-transitgatewayroutetableattachment-transitgatewayroutetablearn"></a>
The ARN of the transit gateway attachment route table\. For example, `"TransitGatewayRouteTableArn": "arn:aws:ec2:us-west-2:123456789012:transit-gateway-route-table/tgw-rtb-9876543210123456"`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `500`  
*Pattern*: `[\s\S]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-networkmanager-transitgatewayroutetableattachment-return-values"></a>

### Ref<a name="aws-resource-networkmanager-transitgatewayroutetableattachment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the attachment ID of the transit gateway route table\. For example: `attachment-12367e74104d31234`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-networkmanager-transitgatewayroutetableattachment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-networkmanager-transitgatewayroutetableattachment-return-values-fn--getatt-fn--getatt"></a>

`AttachmentId`  <a name="AttachmentId-fn::getatt"></a>
The ID of the transit gateway route table attachment\.

`AttachmentPolicyRuleNumber`  <a name="AttachmentPolicyRuleNumber-fn::getatt"></a>
The policy rule number associated with the attachment\.

`AttachmentType`  <a name="AttachmentType-fn::getatt"></a>
The type of attachment\. This will be `TRANSIT_GATEWAY_ROUTE_TABLE`\.

`CoreNetworkArn`  <a name="CoreNetworkArn-fn::getatt"></a>
The ARN of the core network\.

`CoreNetworkId`  <a name="CoreNetworkId-fn::getatt"></a>
The ID of the core network\.

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The timestamp when the transit gateway route table attachment was created\.

`EdgeLocation`  <a name="EdgeLocation-fn::getatt"></a>
The Region where the core network edge is located\.

`OwnerAccountId`  <a name="OwnerAccountId-fn::getatt"></a>
The ID of the transit gateway route table attachment owner\.

`ResourceArn`  <a name="ResourceArn-fn::getatt"></a>
The resource ARN for the transit gateway route table attachment\.

`SegmentName`  <a name="SegmentName-fn::getatt"></a>
The name of the attachment's segment\.

`State`  <a name="State-fn::getatt"></a>
The state of the attachment\. This can be: `REJECTED` \| `PENDING_ATTACHMENT_ACCEPTANCE` \| `CREATING` \| `FAILED` \| `AVAILABLE` \| `UPDATING` \| ` PENDING_NETWORK_UPDATE` \| `PENDING_TAG_ACCEPTANCE` \| `DELETING`\. 

`UpdatedAt`  <a name="UpdatedAt-fn::getatt"></a>
The timestamp when the transit gateway route table attachment was last updated\.