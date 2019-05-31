# AWS::Backup::BackupPlan LifecycleResourceType<a name="aws-properties-backup-backupplan-lifecycleresourcetype"></a>

Specifies an object containing an array of `Transition` objects that determine how long in days before a recovery point transitions to cold storage or is deleted\. 

## Syntax<a name="aws-properties-backup-backupplan-lifecycleresourcetype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-backup-backupplan-lifecycleresourcetype-syntax.json"></a>

```
{
  "[DeleteAfterDays](#cfn-backup-backupplan-lifecycleresourcetype-deleteafterdays)" : Double,
  "[MoveToColdStorageAfterDays](#cfn-backup-backupplan-lifecycleresourcetype-movetocoldstorageafterdays)" : Double
}
```

### YAML<a name="aws-properties-backup-backupplan-lifecycleresourcetype-syntax.yaml"></a>

```
  [DeleteAfterDays](#cfn-backup-backupplan-lifecycleresourcetype-deleteafterdays): Double
  [MoveToColdStorageAfterDays](#cfn-backup-backupplan-lifecycleresourcetype-movetocoldstorageafterdays): Double
```

## Properties<a name="aws-properties-backup-backupplan-lifecycleresourcetype-properties"></a>

`DeleteAfterDays`  <a name="cfn-backup-backupplan-lifecycleresourcetype-deleteafterdays"></a>
Specifies the number of days after creation that a recovery point is deleted\. Must be greater than `MoveToColdStorageAfterDays`\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MoveToColdStorageAfterDays`  <a name="cfn-backup-backupplan-lifecycleresourcetype-movetocoldstorageafterdays"></a>
Specifies the number of days after creation that a recovery point is moved to cold storage\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)