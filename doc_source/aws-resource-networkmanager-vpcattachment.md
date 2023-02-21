# AWS::NetworkManager::VpcAttachment<a name="aws-resource-networkmanager-vpcattachment"></a>

Creates a VPC attachment on an edge location of a core network\.

## Syntax<a name="aws-resource-networkmanager-vpcattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkmanager-vpcattachment-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkManager::VpcAttachment",
  "Properties" : {
      "[CoreNetworkId](#cfn-networkmanager-vpcattachment-corenetworkid)" : String,
      "[Options](#cfn-networkmanager-vpcattachment-options)" : VpcOptions,
      "[SubnetArns](#cfn-networkmanager-vpcattachment-subnetarns)" : [ String, ... ],
      "[Tags](#cfn-networkmanager-vpcattachment-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcArn](#cfn-networkmanager-vpcattachment-vpcarn)" : String
    }
}
```

### YAML<a name="aws-resource-networkmanager-vpcattachment-syntax.yaml"></a>

```
Type: AWS::NetworkManager::VpcAttachment
Properties: 
  [CoreNetworkId](#cfn-networkmanager-vpcattachment-corenetworkid): String
  [Options](#cfn-networkmanager-vpcattachment-options): 
    VpcOptions
  [SubnetArns](#cfn-networkmanager-vpcattachment-subnetarns): 
    - String
  [Tags](#cfn-networkmanager-vpcattachment-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcArn](#cfn-networkmanager-vpcattachment-vpcarn): String
```

## Properties<a name="aws-resource-networkmanager-vpcattachment-properties"></a>

`CoreNetworkId`  <a name="cfn-networkmanager-vpcattachment-corenetworkid"></a>
The core network ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Options`  <a name="cfn-networkmanager-vpcattachment-options"></a>
Options for creating the VPC attachment\.  
*Required*: No  
*Type*: [VpcOptions](aws-properties-networkmanager-vpcattachment-vpcoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetArns`  <a name="cfn-networkmanager-vpcattachment-subnetarns"></a>
The subnet ARNs\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-networkmanager-vpcattachment-tags"></a>
The tags associated with the VPC attachment\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcArn`  <a name="cfn-networkmanager-vpcattachment-vpcarn"></a>
The ARN of the VPC attachment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-networkmanager-vpcattachment-return-values"></a>

### Ref<a name="aws-resource-networkmanager-vpcattachment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `AttachmentId`\. For example, `{ "Ref: "attachment-00067e74104d33769" }`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-networkmanager-vpcattachment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-networkmanager-vpcattachment-return-values-fn--getatt-fn--getatt"></a>

`AttachmentId`  <a name="AttachmentId-fn::getatt"></a>
The ID of the VPC attachment\.

`AttachmentPolicyRuleNumber`  <a name="AttachmentPolicyRuleNumber-fn::getatt"></a>
The policy rule number associated with the attachment\.

`AttachmentType`  <a name="AttachmentType-fn::getatt"></a>
The type of attachment\. This will be `VPC`\.

`CoreNetworkArn`  <a name="CoreNetworkArn-fn::getatt"></a>
The ARN of the core network\. 

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The timestamp when the VPC attachment was created\. 

`EdgeLocation`  <a name="EdgeLocation-fn::getatt"></a>
The Region where the core network edge is located\.

`OwnerAccountId`  <a name="OwnerAccountId-fn::getatt"></a>
The ID of the VPC attachment owner\.

`ProposedSegmentChange`  <a name="ProposedSegmentChange-fn::getatt"></a>
Property description not available\.

`ProposedSegmentChange.AttachmentPolicyRuleNumber`  <a name="ProposedSegmentChange.AttachmentPolicyRuleNumber-fn::getatt"></a>
Property description not available\.

`ProposedSegmentChange.SegmentName`  <a name="ProposedSegmentChange.SegmentName-fn::getatt"></a>
Property description not available\.

`ProposedSegmentChange.Tags`  <a name="ProposedSegmentChange.Tags-fn::getatt"></a>
Property description not available\.

`ResourceArn`  <a name="ResourceArn-fn::getatt"></a>
The resource ARN for the VPC attachment\.

`SegmentName`  <a name="SegmentName-fn::getatt"></a>
The name of the attachment's segment\.

`State`  <a name="State-fn::getatt"></a>
The state of the attachment\. This can be: `REJECTED` \| `PENDING_ATTACHMENT_ACCEPTANCE` \| `CREATING` \| `FAILED` \| `AVAILABLE` \| `UPDATING` \| ` PENDING_NETWORK_UPDATE` \| `PENDING_TAG_ACCEPTANCE` \| `DELETING`\. 

`UpdatedAt`  <a name="UpdatedAt-fn::getatt"></a>
The timestamp when the VPC attachment was last updated\.