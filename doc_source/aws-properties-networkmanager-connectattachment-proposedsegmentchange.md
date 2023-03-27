# AWS::NetworkManager::ConnectAttachment ProposedSegmentChange<a name="aws-properties-networkmanager-connectattachment-proposedsegmentchange"></a>

Describes a proposed segment change\. In some cases, the segment change must first be evaluated and accepted\. 

## Syntax<a name="aws-properties-networkmanager-connectattachment-proposedsegmentchange-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkmanager-connectattachment-proposedsegmentchange-syntax.json"></a>

```
{
  "[AttachmentPolicyRuleNumber](#cfn-networkmanager-connectattachment-proposedsegmentchange-attachmentpolicyrulenumber)" : Integer,
  "[SegmentName](#cfn-networkmanager-connectattachment-proposedsegmentchange-segmentname)" : String,
  "[Tags](#cfn-networkmanager-connectattachment-proposedsegmentchange-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
}
```

### YAML<a name="aws-properties-networkmanager-connectattachment-proposedsegmentchange-syntax.yaml"></a>

```
  [AttachmentPolicyRuleNumber](#cfn-networkmanager-connectattachment-proposedsegmentchange-attachmentpolicyrulenumber): Integer
  [SegmentName](#cfn-networkmanager-connectattachment-proposedsegmentchange-segmentname): String
  [Tags](#cfn-networkmanager-connectattachment-proposedsegmentchange-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-networkmanager-connectattachment-proposedsegmentchange-properties"></a>

`AttachmentPolicyRuleNumber`  <a name="cfn-networkmanager-connectattachment-proposedsegmentchange-attachmentpolicyrulenumber"></a>
The rule number in the policy document that applies to this change\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentName`  <a name="cfn-networkmanager-connectattachment-proposedsegmentchange-segmentname"></a>
The name of the segment to change\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\s\S]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-networkmanager-connectattachment-proposedsegmentchange-tags"></a>
The list of key\-value tags that changed for the segment\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)