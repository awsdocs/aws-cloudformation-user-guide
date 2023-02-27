# AWS::DLM::LifecyclePolicy CrossRegionCopyAction<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyaction"></a>

 **\[Event\-based policies only\]** Specifies a cross\-Region copy action for event\-based policies\.

**Note**  
To specify a cross\-Region copy rule for snapshot and AMI policies, use CrossRegionCopyRule\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyaction-syntax.json"></a>

```
{
  "[EncryptionConfiguration](#cfn-dlm-lifecyclepolicy-crossregioncopyaction-encryptionconfiguration)" : EncryptionConfiguration,
  "[RetainRule](#cfn-dlm-lifecyclepolicy-crossregioncopyaction-retainrule)" : CrossRegionCopyRetainRule,
  "[Target](#cfn-dlm-lifecyclepolicy-crossregioncopyaction-target)" : String
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyaction-syntax.yaml"></a>

```
  [EncryptionConfiguration](#cfn-dlm-lifecyclepolicy-crossregioncopyaction-encryptionconfiguration): 
    EncryptionConfiguration
  [RetainRule](#cfn-dlm-lifecyclepolicy-crossregioncopyaction-retainrule): 
    CrossRegionCopyRetainRule
  [Target](#cfn-dlm-lifecyclepolicy-crossregioncopyaction-target): String
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyaction-properties"></a>

`EncryptionConfiguration`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyaction-encryptionconfiguration"></a>
The encryption settings for the copied snapshot\.  
*Required*: Yes  
*Type*: [EncryptionConfiguration](aws-properties-dlm-lifecyclepolicy-encryptionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetainRule`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyaction-retainrule"></a>
Specifies a retention rule for cross\-Region snapshot copies created by snapshot or event\-based policies, or cross\-Region AMI copies created by AMI policies\. After the retention period expires, the cross\-Region copy is deleted\.  
*Required*: No  
*Type*: [CrossRegionCopyRetainRule](aws-properties-dlm-lifecyclepolicy-crossregioncopyretainrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyaction-target"></a>
The target Region\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Pattern*: `^[\w:\-\/\*]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)