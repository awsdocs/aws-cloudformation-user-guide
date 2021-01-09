# AWS::DLM::LifecyclePolicy CrossRegionCopyAction<a name="aws-properties-dlm-lifecyclepolicy-crossregioncopyaction"></a>

Specifies a rule for copying shared snapshots across Regions\.

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
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [CrossRegionCopyRetainRule](aws-properties-dlm-lifecyclepolicy-crossregioncopyretainrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-dlm-lifecyclepolicy-crossregioncopyaction-target"></a>
The target Region\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `16`  
*Pattern*: `^[\\w:\\-\\/\\*]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)