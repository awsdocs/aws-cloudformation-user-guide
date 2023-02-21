# AWS::DLM::LifecyclePolicy Parameters<a name="aws-properties-dlm-lifecyclepolicy-parameters"></a>

 **\[Snapshot and AMI policies only\]** Specifies optional parameters for snapshot and AMI policies\. The set of valid parameters depends on the combination of policy type and target resource type\.

If you choose to exclude boot volumes and you specify tags that consequently exclude all of the additional data volumes attached to an instance, then Amazon Data Lifecycle Manager will not create any snapshots for the affected instance, and it will emit a `SnapshotsCreateFailed` Amazon CloudWatch metric\. For more information, see [Monitor your policies using Amazon CloudWatch](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/monitor-dlm-cw-metrics.html)\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-parameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-parameters-syntax.json"></a>

```
{
  "[ExcludeBootVolume](#cfn-dlm-lifecyclepolicy-parameters-excludebootvolume)" : Boolean,
  "[ExcludeDataVolumeTags](#cfn-dlm-lifecyclepolicy-parameters-excludedatavolumetags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
  "[NoReboot](#cfn-dlm-lifecyclepolicy-parameters-noreboot)" : Boolean
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-parameters-syntax.yaml"></a>

```
  [ExcludeBootVolume](#cfn-dlm-lifecyclepolicy-parameters-excludebootvolume): Boolean
  [ExcludeDataVolumeTags](#cfn-dlm-lifecyclepolicy-parameters-excludedatavolumetags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [NoReboot](#cfn-dlm-lifecyclepolicy-parameters-noreboot): Boolean
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-parameters-properties"></a>

`ExcludeBootVolume`  <a name="cfn-dlm-lifecyclepolicy-parameters-excludebootvolume"></a>
 **\[Snapshot policies that target instances only\]** Indicates whether to exclude the root volume from multi\-volume snapshot sets\. The default is `false`\. If you specify `true`, then the root volumes attached to targeted instances will be excluded from the multi\-volume snapshot sets created by the policy\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeDataVolumeTags`  <a name="cfn-dlm-lifecyclepolicy-parameters-excludedatavolumetags"></a>
 **\[Snapshot policies that target instances only\]** The tags used to identify data \(non\-root\) volumes to exclude from multi\-volume snapshot sets\.  
If you create a snapshot lifecycle policy that targets instances and you specify tags for this parameter, then data volumes with the specified tags that are attached to targeted instances will be excluded from the multi\-volume snapshot sets created by the policy\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoReboot`  <a name="cfn-dlm-lifecyclepolicy-parameters-noreboot"></a>
 **\[AMI policies only\]** Indicates whether targeted instances are rebooted when the lifecycle policy runs\. `true` indicates that targeted instances are not rebooted when the policy runs\. `false` indicates that target instances are rebooted when the policy runs\. The default is `true` \(instances are not rebooted\)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)