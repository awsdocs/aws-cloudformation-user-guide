# AWS::DLM::LifecyclePolicy ArchiveRetainRule<a name="aws-properties-dlm-lifecyclepolicy-archiveretainrule"></a>

 **\[Snapshot policies only\]** Specifies information about the archive storage tier retention period\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-archiveretainrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-archiveretainrule-syntax.json"></a>

```
{
  "[RetentionArchiveTier](#cfn-dlm-lifecyclepolicy-archiveretainrule-retentionarchivetier)" : RetentionArchiveTier
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-archiveretainrule-syntax.yaml"></a>

```
  [RetentionArchiveTier](#cfn-dlm-lifecyclepolicy-archiveretainrule-retentionarchivetier): 
    RetentionArchiveTier
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-archiveretainrule-properties"></a>

`RetentionArchiveTier`  <a name="cfn-dlm-lifecyclepolicy-archiveretainrule-retentionarchivetier"></a>
Information about retention period in the Amazon EBS Snapshots Archive\. For more information, see [Archive Amazon EBS snapshots](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/snapshot-archive.html)\.  
*Required*: Yes  
*Type*: [RetentionArchiveTier](aws-properties-dlm-lifecyclepolicy-retentionarchivetier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)