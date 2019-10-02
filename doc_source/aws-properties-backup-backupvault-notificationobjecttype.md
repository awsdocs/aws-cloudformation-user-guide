# AWS::Backup::BackupVault NotificationObjectType<a name="aws-properties-backup-backupvault-notificationobjecttype"></a>

Specifies an object containing SNS event notification properties for the target backup vault\.

## Syntax<a name="aws-properties-backup-backupvault-notificationobjecttype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-backup-backupvault-notificationobjecttype-syntax.json"></a>

```
{
  "[BackupVaultEvents](#cfn-backup-backupvault-notificationobjecttype-backupvaultevents)" : [ String, ... ],
  "[SNSTopicArn](#cfn-backup-backupvault-notificationobjecttype-snstopicarn)" : String
}
```

### YAML<a name="aws-properties-backup-backupvault-notificationobjecttype-syntax.yaml"></a>

```
  [BackupVaultEvents](#cfn-backup-backupvault-notificationobjecttype-backupvaultevents): 
    - String
  [SNSTopicArn](#cfn-backup-backupvault-notificationobjecttype-snstopicarn): String
```

## Properties<a name="aws-properties-backup-backupvault-notificationobjecttype-properties"></a>

`BackupVaultEvents`  <a name="cfn-backup-backupvault-notificationobjecttype-backupvaultevents"></a>
An array of events that indicate the status of jobs to back up resources to the backup vault\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SNSTopicArn`  <a name="cfn-backup-backupvault-notificationobjecttype-snstopicarn"></a>
An ARN that uniquely identifies an Amazon Simple Notification Service \(Amazon SNS\) topic; for example, `arn:aws:sns:us-west-2:111122223333:MyTopic`\.  
*Required*: Yes  
*Type*: String  
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
