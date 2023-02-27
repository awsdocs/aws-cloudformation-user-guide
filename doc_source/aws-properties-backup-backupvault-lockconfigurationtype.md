# AWS::Backup::BackupVault LockConfigurationType<a name="aws-properties-backup-backupvault-lockconfigurationtype"></a>

The `LockConfigurationType` property type specifies configuration for [AWS Backup Vault Lock](https://docs.aws.amazon.com/aws-backup/latest/devguide/vault-lock.html)\.

## Syntax<a name="aws-properties-backup-backupvault-lockconfigurationtype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-backup-backupvault-lockconfigurationtype-syntax.json"></a>

```
{
  "[ChangeableForDays](#cfn-backup-backupvault-lockconfigurationtype-changeablefordays)" : Integer,
  "[MaxRetentionDays](#cfn-backup-backupvault-lockconfigurationtype-maxretentiondays)" : Integer,
  "[MinRetentionDays](#cfn-backup-backupvault-lockconfigurationtype-minretentiondays)" : Integer
}
```

### YAML<a name="aws-properties-backup-backupvault-lockconfigurationtype-syntax.yaml"></a>

```
  [ChangeableForDays](#cfn-backup-backupvault-lockconfigurationtype-changeablefordays): Integer
  [MaxRetentionDays](#cfn-backup-backupvault-lockconfigurationtype-maxretentiondays): Integer
  [MinRetentionDays](#cfn-backup-backupvault-lockconfigurationtype-minretentiondays): Integer
```

## Properties<a name="aws-properties-backup-backupvault-lockconfigurationtype-properties"></a>

`ChangeableForDays`  <a name="cfn-backup-backupvault-lockconfigurationtype-changeablefordays"></a>
The AWS Backup Vault Lock configuration that specifies the number of days before the lock date\. For example, setting `ChangeableForDays` to 30 on Jan\. 1, 2022 at 8pm UTC will set the lock date to Jan\. 31, 2022 at 8pm UTC\.  
AWS Backup enforces a 72\-hour cooling\-off period before Vault Lock takes effect and becomes immutable\. Therefore, you must set `ChangeableForDays` to 3 or greater\.  
Before the lock date, you can delete Vault Lock from the vault using `DeleteBackupVaultLockConfiguration` or change the Vault Lock configuration using `PutBackupVaultLockConfiguration`\. On and after the lock date, the Vault Lock becomes immutable and cannot be changed or deleted\.  
If this parameter is not specified, you can delete Vault Lock from the vault using `DeleteBackupVaultLockConfiguration` or change the Vault Lock configuration using `PutBackupVaultLockConfiguration` at any time\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxRetentionDays`  <a name="cfn-backup-backupvault-lockconfigurationtype-maxretentiondays"></a>
The AWS Backup Vault Lock configuration that specifies the maximum retention period that the vault retains its recovery points\. This setting can be useful if, for example, your organization's policies require you to destroy certain data after retaining it for four years \(1460 days\)\.  
If this parameter is not included, Vault Lock does not enforce a maximum retention period on the recovery points in the vault\. If this parameter is included without a value, Vault Lock will not enforce a maximum retention period\.  
If this parameter is specified, any backup or copy job to the vault must have a lifecycle policy with a retention period equal to or shorter than the maximum retention period\. If the job's retention period is longer than that maximum retention period, then the vault fails the backup or copy job, and you should either modify your lifecycle settings or use a different vault\. Recovery points already saved in the vault prior to Vault Lock are not affected\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinRetentionDays`  <a name="cfn-backup-backupvault-lockconfigurationtype-minretentiondays"></a>
The AWS Backup Vault Lock configuration that specifies the minimum retention period that the vault retains its recovery points\. This setting can be useful if, for example, your organization's policies require you to retain certain data for at least seven years \(2555 days\)\.  
If this parameter is not specified, Vault Lock will not enforce a minimum retention period\.  
If this parameter is specified, any backup or copy job to the vault must have a lifecycle policy with a retention period equal to or longer than the minimum retention period\. If the job's retention period is shorter than that minimum retention period, then the vault fails that backup or copy job, and you should either modify your lifecycle settings or use a different vault\. Recovery points already saved in the vault prior to Vault Lock are not affected\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)