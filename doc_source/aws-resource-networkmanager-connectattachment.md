# AWS::NetworkManager::ConnectAttachment<a name="aws-resource-networkmanager-connectattachment"></a>

Creates a core network Connect attachment from a specified core network attachment\. 

A core network Connect attachment is a GRE\-based tunnel attachment that you can use to establish a connection between a core network and an appliance\. A core network Connect attachment uses an existing VPC attachment as the underlying transport mechanism\.

## Syntax<a name="aws-resource-networkmanager-connectattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkmanager-connectattachment-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkManager::ConnectAttachment",
  "Properties" : {
      "[CoreNetworkId](#cfn-networkmanager-connectattachment-corenetworkid)" : String,
      "[EdgeLocation](#cfn-networkmanager-connectattachment-edgelocation)" : String,
      "[Options](#cfn-networkmanager-connectattachment-options)" : ConnectAttachmentOptions,
      "[Tags](#cfn-networkmanager-connectattachment-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TransportAttachmentId](#cfn-networkmanager-connectattachment-transportattachmentid)" : String
    }
}
```

### YAML<a name="aws-resource-networkmanager-connectattachment-syntax.yaml"></a>

```
Type: AWS::NetworkManager::ConnectAttachment
Properties: 
  [CoreNetworkId](#cfn-networkmanager-connectattachment-corenetworkid): String
  [EdgeLocation](#cfn-networkmanager-connectattachment-edgelocation): String
  [Options](#cfn-networkmanager-connectattachment-options): 
    ConnectAttachmentOptions
  [Tags](#cfn-networkmanager-connectattachment-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TransportAttachmentId](#cfn-networkmanager-connectattachment-transportattachmentid): String
```

## Properties<a name="aws-resource-networkmanager-connectattachment-properties"></a>

`CoreNetworkId`  <a name="cfn-networkmanager-connectattachment-corenetworkid"></a>
The ID of the core network where the Connect attachment is located\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EdgeLocation`  <a name="cfn-networkmanager-connectattachment-edgelocation"></a>
The Region where the edge is located\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `[\s\S]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Options`  <a name="cfn-networkmanager-connectattachment-options"></a>
Options for connecting an attachment\.  
*Required*: Yes  
*Type*: [ConnectAttachmentOptions](aws-properties-networkmanager-connectattachment-connectattachmentoptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-networkmanager-connectattachment-tags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransportAttachmentId`  <a name="cfn-networkmanager-connectattachment-transportattachmentid"></a>
The ID of the transport attachment\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `50`  
*Pattern*: `^attachment-([0-9a-f]{8,17})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-networkmanager-connectattachment-return-values"></a>

### Ref<a name="aws-resource-networkmanager-connectattachment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `AttachmentId`\. For example, `{ "Ref: "attachment-02767e74104a33690" }`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-networkmanager-connectattachment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-networkmanager-connectattachment-return-values-fn--getatt-fn--getatt"></a>

`AttachmentId`  <a name="AttachmentId-fn::getatt"></a>
The ID of the Connect attachment\.

`AttachmentPolicyRuleNumber`  <a name="AttachmentPolicyRuleNumber-fn::getatt"></a>
The rule number associated with the attachment\.

`AttachmentType`  <a name="AttachmentType-fn::getatt"></a>
The type of attachment\. This will be `CONNECT`\.

`CoreNetworkArn`  <a name="CoreNetworkArn-fn::getatt"></a>
The ARN of the core network\.

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The timestamp when the Connect attachment was created\.

`OwnerAccountId`  <a name="OwnerAccountId-fn::getatt"></a>
The ID of the Connect attachment owner\.

`ProposedSegmentChange`  <a name="ProposedSegmentChange-fn::getatt"></a>
Property description not available\.

`ProposedSegmentChange.AttachmentPolicyRuleNumber`  <a name="ProposedSegmentChange.AttachmentPolicyRuleNumber-fn::getatt"></a>
Property description not available\.

`ProposedSegmentChange.SegmentName`  <a name="ProposedSegmentChange.SegmentName-fn::getatt"></a>
Property description not available\.

`ProposedSegmentChange.Tags`  <a name="ProposedSegmentChange.Tags-fn::getatt"></a>
Property description not available\.

`ResourceArn`  <a name="ResourceArn-fn::getatt"></a>
The resource ARN for the Connect attachment\.

`SegmentName`  <a name="SegmentName-fn::getatt"></a>
The name of the Connect attachment's segment\.

`State`  <a name="State-fn::getatt"></a>
The state of the Connect attachment\. This can be: `REJECTED` \| `PENDING_ATTACHMENT_ACCEPTANCE` \| `CREATING` \| `FAILED` \| `AVAILABLE` \| `UPDATING` \| ` PENDING_NETWORK_UPDATE` \| `PENDING_TAG_ACCEPTANCE` \| `DELETING`\. 

`UpdatedAt`  <a name="UpdatedAt-fn::getatt"></a>
The timestamp when the Connect attachment was last updated\.