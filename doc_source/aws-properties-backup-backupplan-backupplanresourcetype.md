# AWS::Backup::BackupPlan BackupPlanResourceType<a name="aws-properties-backup-backupplan-backupplanresourcetype"></a>

Specifies an object containing properties used to create a backup plan\.

## Syntax<a name="aws-properties-backup-backupplan-backupplanresourcetype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-backup-backupplan-backupplanresourcetype-syntax.json"></a>

```
{
  "[BackupPlanName](#cfn-backup-backupplan-backupplanresourcetype-backupplanname)" : String,
  "[BackupPlanRule](#cfn-backup-backupplan-backupplanresourcetype-backupplanrule)" : [ [BackupRuleResourceType](aws-properties-backup-backupplan-backupruleresourcetype.md), ... ]
}
```

### YAML<a name="aws-properties-backup-backupplan-backupplanresourcetype-syntax.yaml"></a>

```
  [BackupPlanName](#cfn-backup-backupplan-backupplanresourcetype-backupplanname): String
  [BackupPlanRule](#cfn-backup-backupplan-backupplanresourcetype-backupplanrule): 
    - [BackupRuleResourceType](aws-properties-backup-backupplan-backupruleresourcetype.md)
```

## Properties<a name="aws-properties-backup-backupplan-backupplanresourcetype-properties"></a>

`BackupPlanName`  <a name="cfn-backup-backupplan-backupplanresourcetype-backupplanname"></a>
The display name of a backup plan\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BackupPlanRule`  <a name="cfn-backup-backupplan-backupplanresourcetype-backupplanrule"></a>
An array of `BackupRule` objects, each of which specifies a scheduled task that is used to back up a selection of resources\.  
*Required*: Yes  
*Type*: List of [BackupRuleResourceType](aws-properties-backup-backupplan-backupruleresourcetype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
