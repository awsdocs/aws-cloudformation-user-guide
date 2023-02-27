# AWS::DLM::LifecyclePolicy Schedule<a name="aws-properties-dlm-lifecyclepolicy-schedule"></a>

 **\[Snapshot and AMI policies only\]** Specifies a schedule for a snapshot or AMI lifecycle policy\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-schedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-schedule-syntax.json"></a>

```
{
  "[ArchiveRule](#cfn-dlm-lifecyclepolicy-schedule-archiverule)" : ArchiveRule,
  "[CopyTags](#cfn-dlm-lifecyclepolicy-schedule-copytags)" : Boolean,
  "[CreateRule](#cfn-dlm-lifecyclepolicy-schedule-createrule)" : CreateRule,
  "[CrossRegionCopyRules](#cfn-dlm-lifecyclepolicy-schedule-crossregioncopyrules)" : [ CrossRegionCopyRule, ... ],
  "[DeprecateRule](#cfn-dlm-lifecyclepolicy-schedule-deprecaterule)" : DeprecateRule,
  "[FastRestoreRule](#cfn-dlm-lifecyclepolicy-schedule-fastrestorerule)" : FastRestoreRule,
  "[Name](#cfn-dlm-lifecyclepolicy-schedule-name)" : String,
  "[RetainRule](#cfn-dlm-lifecyclepolicy-schedule-retainrule)" : RetainRule,
  "[ShareRules](#cfn-dlm-lifecyclepolicy-schedule-sharerules)" : [ ShareRule, ... ],
  "[TagsToAdd](#cfn-dlm-lifecyclepolicy-schedule-tagstoadd)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
  "[VariableTags](#cfn-dlm-lifecyclepolicy-schedule-variabletags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-schedule-syntax.yaml"></a>

```
  [ArchiveRule](#cfn-dlm-lifecyclepolicy-schedule-archiverule): 
    ArchiveRule
  [CopyTags](#cfn-dlm-lifecyclepolicy-schedule-copytags): Boolean
  [CreateRule](#cfn-dlm-lifecyclepolicy-schedule-createrule): 
    CreateRule
  [CrossRegionCopyRules](#cfn-dlm-lifecyclepolicy-schedule-crossregioncopyrules): 
    - CrossRegionCopyRule
  [DeprecateRule](#cfn-dlm-lifecyclepolicy-schedule-deprecaterule): 
    DeprecateRule
  [FastRestoreRule](#cfn-dlm-lifecyclepolicy-schedule-fastrestorerule): 
    FastRestoreRule
  [Name](#cfn-dlm-lifecyclepolicy-schedule-name): String
  [RetainRule](#cfn-dlm-lifecyclepolicy-schedule-retainrule): 
    RetainRule
  [ShareRules](#cfn-dlm-lifecyclepolicy-schedule-sharerules): 
    - ShareRule
  [TagsToAdd](#cfn-dlm-lifecyclepolicy-schedule-tagstoadd): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VariableTags](#cfn-dlm-lifecyclepolicy-schedule-variabletags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-schedule-properties"></a>

`ArchiveRule`  <a name="cfn-dlm-lifecyclepolicy-schedule-archiverule"></a>
 **\[Snapshot policies that target volumes only\]** The snapshot archiving rule for the schedule\. When you specify an archiving rule, snapshots are automatically moved from the standard tier to the archive tier once the schedule's retention threshold is met\. Snapshots are then retained in the archive tier for the archive retention period that you specify\.   
For more information about using snapshot archiving, see [Considerations for snapshot lifecycle policies](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/snapshot-ami-policy.html#dlm-archive)\.  
*Required*: No  
*Type*: [ArchiveRule](aws-properties-dlm-lifecyclepolicy-archiverule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CopyTags`  <a name="cfn-dlm-lifecyclepolicy-schedule-copytags"></a>
Copy all user\-defined tags on a source volume to snapshots of the volume created by this policy\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreateRule`  <a name="cfn-dlm-lifecyclepolicy-schedule-createrule"></a>
The creation rule\.  
*Required*: No  
*Type*: [CreateRule](aws-properties-dlm-lifecyclepolicy-createrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CrossRegionCopyRules`  <a name="cfn-dlm-lifecyclepolicy-schedule-crossregioncopyrules"></a>
Specifies a rule for copying snapshots or AMIs across regions\.  
You can't specify cross\-Region copy rules for policies that create snapshots on an Outpost\. If the policy creates snapshots in a Region, then snapshots can be copied to up to three Regions or Outposts\.
*Required*: No  
*Type*: List of [CrossRegionCopyRule](aws-properties-dlm-lifecyclepolicy-crossregioncopyrule.md)  
*Maximum*: `3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeprecateRule`  <a name="cfn-dlm-lifecyclepolicy-schedule-deprecaterule"></a>
 **\[AMI policies only\]** The AMI deprecation rule for the schedule\.  
*Required*: No  
*Type*: [DeprecateRule](aws-properties-dlm-lifecyclepolicy-deprecaterule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FastRestoreRule`  <a name="cfn-dlm-lifecyclepolicy-schedule-fastrestorerule"></a>
 **\[Snapshot policies only\]** The rule for enabling fast snapshot restore\.  
*Required*: No  
*Type*: [FastRestoreRule](aws-properties-dlm-lifecyclepolicy-fastrestorerule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-dlm-lifecyclepolicy-schedule-name"></a>
The name of the schedule\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `120`  
*Pattern*: `[0-9A-Za-z _-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetainRule`  <a name="cfn-dlm-lifecyclepolicy-schedule-retainrule"></a>
The retention rule for snapshots or AMIs created by the policy\.  
*Required*: No  
*Type*: [RetainRule](aws-properties-dlm-lifecyclepolicy-retainrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShareRules`  <a name="cfn-dlm-lifecyclepolicy-schedule-sharerules"></a>
 **\[Snapshot policies only\]** The rule for sharing snapshots with other AWS accounts\.  
*Required*: No  
*Type*: List of [ShareRule](aws-properties-dlm-lifecyclepolicy-sharerule.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagsToAdd`  <a name="cfn-dlm-lifecyclepolicy-schedule-tagstoadd"></a>
The tags to apply to policy\-created resources\. These user\-defined tags are in addition to the AWS\-added lifecycle tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `45`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VariableTags`  <a name="cfn-dlm-lifecyclepolicy-schedule-variabletags"></a>
 **\[AMI policies and snapshot policies that target instances only\]** A collection of key/value pairs with values determined dynamically when the policy is executed\. Keys may be any valid Amazon EC2 tag key\. Values must be in one of the two following formats: `$(instance-id)` or `$(timestamp)`\. Variable tags are only valid for EBS Snapshot Management – Instance policies\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `45`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)