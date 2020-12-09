# AWS::Backup::BackupPlan AdvancedBackupSettingResourceType<a name="aws-properties-backup-backupplan-advancedbackupsettingresourcetype"></a>

Specifies an object containing resource type and backup options\. This is only Supported for Windows VSS Backups\.

## Syntax<a name="aws-properties-backup-backupplan-advancedbackupsettingresourcetype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-backup-backupplan-advancedbackupsettingresourcetype-syntax.json"></a>

```
{
  "[BackupOptions](#cfn-backup-backupplan-advancedbackupsettingresourcetype-backupoptions)" : Json,
  "[ResourceType](#cfn-backup-backupplan-advancedbackupsettingresourcetype-resourcetype)" : String
}
```

### YAML<a name="aws-properties-backup-backupplan-advancedbackupsettingresourcetype-syntax.yaml"></a>

```
  [BackupOptions](#cfn-backup-backupplan-advancedbackupsettingresourcetype-backupoptions): Json
  [ResourceType](#cfn-backup-backupplan-advancedbackupsettingresourcetype-resourcetype): String
```

## Properties<a name="aws-properties-backup-backupplan-advancedbackupsettingresourcetype-properties"></a>

`BackupOptions`  <a name="cfn-backup-backupplan-advancedbackupsettingresourcetype-backupoptions"></a>
The backup option for the resource\. Each option is a key\-value pair\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceType`  <a name="cfn-backup-backupplan-advancedbackupsettingresourcetype-resourcetype"></a>
The name of a resource type\. The only supported resource type is EC2\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)