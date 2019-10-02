# AWS::Backup::BackupVault<a name="aws-resource-backup-backupvault"></a>

Creates a logical container where backups are stored\. A `CreateBackupVault` request includes a name, optionally one or more resource tags, an encryption key, and a request ID\.

**Note**  
Sensitive data, such as passport numbers, should not be included the name of a backup vault\.

## Syntax<a name="aws-resource-backup-backupvault-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-backup-backupvault-syntax.json"></a>

```
{
  "Type" : "AWS::Backup::BackupVault",
  "Properties" : {
      "[AccessPolicy](#cfn-backup-backupvault-accesspolicy)" : Json,
      "[BackupVaultName](#cfn-backup-backupvault-backupvaultname)" : String,
      "[BackupVaultTags](#cfn-backup-backupvault-backupvaulttags)" : Json,
      "[EncryptionKeyArn](#cfn-backup-backupvault-encryptionkeyarn)" : String,
      "[Notifications](#cfn-backup-backupvault-notifications)" : [NotificationObjectType](aws-properties-backup-backupvault-notificationobjecttype.md)
    }
}
```

### YAML<a name="aws-resource-backup-backupvault-syntax.yaml"></a>

```
Type: AWS::Backup::BackupVault
Properties: 
  [AccessPolicy](#cfn-backup-backupvault-accesspolicy): Json
  [BackupVaultName](#cfn-backup-backupvault-backupvaultname): String
  [BackupVaultTags](#cfn-backup-backupvault-backupvaulttags): Json
  [EncryptionKeyArn](#cfn-backup-backupvault-encryptionkeyarn): String
  [Notifications](#cfn-backup-backupvault-notifications): 
    [NotificationObjectType](aws-properties-backup-backupvault-notificationobjecttype.md)
```

## Properties<a name="aws-resource-backup-backupvault-properties"></a>

`AccessPolicy`  <a name="cfn-backup-backupvault-accesspolicy"></a>
A resource\-based policy that is used to manage access permissions on the target backup vault\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BackupVaultName`  <a name="cfn-backup-backupvault-backupvaultname"></a>
The name of a logical container where backups are stored\. Backup vaults are identified by names that are unique to the account used to create them and the AWS Region where they are created\. They consist of lowercase letters, numbers, and hyphens\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^[a-zA-Z0-9\-\_\.]{1,50}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BackupVaultTags`  <a name="cfn-backup-backupvault-backupvaulttags"></a>
Metadata that you can assign to help organize the resources that you create\. Each tag is a key\-value pair\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionKeyArn`  <a name="cfn-backup-backupvault-encryptionkeyarn"></a>
The server\-side encryption key that is used to protect your backups; for example, `arn:aws:kms:us-west-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Notifications`  <a name="cfn-backup-backupvault-notifications"></a>
The SNS event notifications for the specified backup vault\.  
*Required*: No  
*Type*: [NotificationObjectType](aws-properties-backup-backupvault-notificationobjecttype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-backup-backupvault-return-values"></a>

### Ref<a name="aws-resource-backup-backupvault-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns `BackupVaultName`\.

### Fn::GetAtt<a name="aws-resource-backup-backupvault-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-backup-backupvault-return-values-fn--getatt-fn--getatt"></a>

`BackupVaultArn`  <a name="BackupVaultArn-fn::getatt"></a>
An Amazon Resource Name \(ARN\) that uniquely identifies a backup vault; for example, `arn:aws:backup:us-east-1:123456789012:vault:aBackupVault`\.

`BackupVaultName`  <a name="BackupVaultName-fn::getatt"></a>
The name of a logical container where backups are stored\. Backup vaults are identified by names that are unique to the account used to create them and the Region where they are created\. They consist of lowercase letters, numbers, and hyphens\.

## Supported Regions

This ResourceType is supported by the following regions:

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
