# AWS::DLM::LifecyclePolicy ArchiveRule<a name="aws-properties-dlm-lifecyclepolicy-archiverule"></a>

 **\[Snapshot policies only\]** Specifies a snapshot archiving rule for a schedule\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-archiverule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-archiverule-syntax.json"></a>

```
{
  "[RetainRule](#cfn-dlm-lifecyclepolicy-archiverule-retainrule)" : ArchiveRetainRule
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-archiverule-syntax.yaml"></a>

```
  [RetainRule](#cfn-dlm-lifecyclepolicy-archiverule-retainrule): 
    ArchiveRetainRule
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-archiverule-properties"></a>

`RetainRule`  <a name="cfn-dlm-lifecyclepolicy-archiverule-retainrule"></a>
Information about the retention period for the snapshot archiving rule\.  
*Required*: Yes  
*Type*: [ArchiveRetainRule](aws-properties-dlm-lifecyclepolicy-archiveretainrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)