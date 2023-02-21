# AWS::DLM::LifecyclePolicy CrossRegionCopyRule<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyrule"></a>

 **\[Snapshot and AMI policies only\]** Specifies a cross\-Region copy rule for snapshot and AMI policies\.

**Note**  
To specify a cross\-Region copy action for event\-based polices, use CrossRegionCopyAction\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyrule-syntax.json"></a>

```
{
  "[CmkArn](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-cmkarn)" : String,
  "[CopyTags](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-copytags)" : Boolean,
  "[DeprecateRule](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-deprecaterule)" : CrossRegionCopyDeprecateRule,
  "[Encrypted](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-encrypted)" : Boolean,
  "[RetainRule](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-retainrule)" : CrossRegionCopyRetainRule,
  "[Target](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-target)" : String,
  "[TargetRegion](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-targetregion)" : String
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyrule-syntax.yaml"></a>

```
  [CmkArn](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-cmkarn): String
  [CopyTags](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-copytags): Boolean
  [DeprecateRule](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-deprecaterule): 
    CrossRegionCopyDeprecateRule
  [Encrypted](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-encrypted): Boolean
  [RetainRule](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-retainrule): 
    CrossRegionCopyRetainRule
  [Target](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-target): String
  [TargetRegion](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-targetregion): String
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyrule-properties"></a>

`CmkArn`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyrule-cmkarn"></a>
The Amazon Resource Name \(ARN\) of the AWS KMS key to use for EBS encryption\. If this parameter is not specified, the default KMS key for the account is used\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Pattern*: `arn:aws(-[a-z]{1,3}){0,2}:kms:([a-z]+-){2,3}\d:\d+:key/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CopyTags`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyrule-copytags"></a>
Indicates whether to copy all user\-defined tags from the source snapshot or AMI to the cross\-Region copy\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeprecateRule`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyrule-deprecaterule"></a>
 **\[AMI policies only\]** The AMI deprecation rule for cross\-Region AMI copies created by the rule\.  
*Required*: No  
*Type*: [CrossRegionCopyDeprecateRule](aws-properties-dlm-lifecyclepolicy-crossregioncopydeprecaterule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encrypted`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyrule-encrypted"></a>
To encrypt a copy of an unencrypted snapshot if encryption by default is not enabled, enable encryption using this parameter\. Copies of encrypted snapshots are encrypted, even if this parameter is false or if encryption by default is not enabled\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetainRule`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyrule-retainrule"></a>
The retention rule that indicates how long the cross\-Region snapshot or AMI copies are to be retained in the destination Region\.  
*Required*: No  
*Type*: [CrossRegionCopyRetainRule](aws-properties-dlm-lifecyclepolicy-crossregioncopyretainrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyrule-target"></a>
The target Region or the Amazon Resource Name \(ARN\) of the target Outpost for the snapshot copies\.  
Use this parameter instead of **TargetRegion**\. Do not specify both\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Pattern*: `^[\w:\-\/\*]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetRegion`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyrule-targetregion"></a>
Avoid using this parameter when creating new policies\. Instead, use **Target** to specify a target Region or a target Outpost for snapshot copies\.  
For policies created before the **Target** parameter was introduced, this parameter indicates the target Region for snapshot copies\.
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `16`  
*Pattern*: `([a-z]+-){2,3}\d`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)