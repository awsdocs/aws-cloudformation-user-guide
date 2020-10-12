# AWS::Backup::BackupPlan CopyActionResourceType<a name="aws-properties-backup-backupplan-copyactionresourcetype"></a>

Copies backups created by a backup rule to another vault\.

## Syntax<a name="aws-properties-backup-backupplan-copyactionresourcetype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-backup-backupplan-copyactionresourcetype-syntax.json"></a>

```
{
  "[DestinationBackupVaultArn](#cfn-backup-backupplan-copyactionresourcetype-destinationbackupvaultarn)" : String,
  "[Lifecycle](#cfn-backup-backupplan-copyactionresourcetype-lifecycle)" : LifecycleResourceType
}
```

### YAML<a name="aws-properties-backup-backupplan-copyactionresourcetype-syntax.yaml"></a>

```
  [DestinationBackupVaultArn](#cfn-backup-backupplan-copyactionresourcetype-destinationbackupvaultarn): String
  [Lifecycle](#cfn-backup-backupplan-copyactionresourcetype-lifecycle): 
    LifecycleResourceType
```

## Properties<a name="aws-properties-backup-backupplan-copyactionresourcetype-properties"></a>

`DestinationBackupVaultArn`  <a name="cfn-backup-backupplan-copyactionresourcetype-destinationbackupvaultarn"></a>
An Amazon Resource Name \(ARN\) that uniquely identifies the destination backup vault for the copied backup\. For example, `arn:aws:backup:us-east-1:123456789012:vault:aBackupVault.`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Lifecycle`  <a name="cfn-backup-backupplan-copyactionresourcetype-lifecycle"></a>
Defines when a protected resource is transitioned to cold storage and when it expires\. AWS Backup transitions and expires backups automatically according to the lifecycle that you define\. If you do not specify a lifecycle, AWS Backup applies the lifecycle policy of the source backup to the destination backup\.  
Backups transitioned to cold storage must be stored in cold storage for a minimum of 90 days\.  
*Required*: No  
*Type*: [LifecycleResourceType](aws-properties-backup-backupplan-lifecycleresourcetype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)