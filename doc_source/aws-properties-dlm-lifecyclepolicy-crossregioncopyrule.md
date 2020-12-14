# AWS::DLM::LifecyclePolicy CrossRegionCopyRule<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyrule"></a>

Specifies a rule for cross\-Region snapshot copies\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyrule-syntax.json"></a>

```
{
  "[CmkArn](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-cmkarn)" : String,
  "[CopyTags](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-copytags)" : Boolean,
  "[Encrypted](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-encrypted)" : Boolean,
  "[RetainRule](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-retainrule)" : CrossRegionCopyRetainRule,
  "[TargetRegion](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-targetregion)" : String
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyrule-syntax.yaml"></a>

```
  [CmkArn](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-cmkarn): String
  [CopyTags](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-copytags): Boolean
  [Encrypted](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-encrypted): Boolean
  [RetainRule](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-retainrule): 
    CrossRegionCopyRetainRule
  [TargetRegion](#cfn-dlm-lifecyclepolicy-crossregioncopyrule-targetregion): String
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyrule-properties"></a>

`CmkArn`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyrule-cmkarn"></a>
The Amazon Resource Name \(ARN\) of the AWS KMS customer master key \(CMK\) to use for EBS encryption\. If this parameter is not specified, your AWS managed CMK for EBS is used\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Pattern*: `arn:aws(-[a-z]{1,3}){0,2}:kms:([a-z]+-){2,3}\d:\d+:key/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CopyTags`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyrule-copytags"></a>
Copy all user\-defined tags from the source snapshot to the copied snapshot\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encrypted`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyrule-encrypted"></a>
To encrypt a copy of an unencrypted snapshot if encryption by default is not enabled, enable encryption using this parameter\. Copies of encrypted snapshots are encrypted, even if this parameter is false or if encryption by default is not enabled\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetainRule`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyrule-retainrule"></a>
The retention rule\.  
*Required*: No  
*Type*: [CrossRegionCopyRetainRule](aws-properties-dlm-lifecyclepolicy-crossregioncopyretainrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetRegion`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyrule-targetregion"></a>
The target Region\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `16`  
*Pattern*: `([a-z]+-){2,3}\d`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)