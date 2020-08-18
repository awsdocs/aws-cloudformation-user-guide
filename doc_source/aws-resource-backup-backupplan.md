# AWS::Backup::BackupPlan<a name="aws-resource-backup-backupplan"></a>

Contains an optional backup plan display name and an array of `BackupRule` objects, each of which specifies a backup rule\. Each rule in a backup plan is a separate scheduled task and can back up a different selection of AWS resources\.

## Syntax<a name="aws-resource-backup-backupplan-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-backup-backupplan-syntax.json"></a>

```
{
  "Type" : "AWS::Backup::BackupPlan",
  "Properties" : {
      "[BackupPlan](#cfn-backup-backupplan-backupplan)" : BackupPlanResourceType,
      "[BackupPlanTags](#cfn-backup-backupplan-backupplantags)" : Json
    }
}
```

### YAML<a name="aws-resource-backup-backupplan-syntax.yaml"></a>

```
Type: AWS::Backup::BackupPlan
Properties: 
  [BackupPlan](#cfn-backup-backupplan-backupplan): 
    BackupPlanResourceType
  [BackupPlanTags](#cfn-backup-backupplan-backupplantags): Json
```

## Properties<a name="aws-resource-backup-backupplan-properties"></a>

`BackupPlan`  <a name="cfn-backup-backupplan-backupplan"></a>
Uniquely identifies the backup plan to be associated with the selection of resources\.  
*Required*: Yes  
*Type*: [BackupPlanResourceType](aws-properties-backup-backupplan-backupplanresourcetype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BackupPlanTags`  <a name="cfn-backup-backupplan-backupplantags"></a>
To help organize your resources, you can assign your own metadata to the resources that you create\. Each tag is a key\-value pair\. The specified tags are assigned to all backups created with this plan\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-backup-backupplan-return-values"></a>

### Ref<a name="aws-resource-backup-backupplan-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns `BackupPlanId`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-backup-backupplan-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-backup-backupplan-return-values-fn--getatt-fn--getatt"></a>

`BackupPlanArn`  <a name="BackupPlanArn-fn::getatt"></a>
An Amazon Resource Name \(ARN\) that uniquely identifies a backup plan; for example, `arn:aws:backup:us-east-1:123456789012:plan:8F81F553-3A74-4A3F-B93D-B3360DC80C50`\.

`BackupPlanId`  <a name="BackupPlanId-fn::getatt"></a>
Uniquely identifies a backup plan\.

`VersionId`  <a name="VersionId-fn::getatt"></a>
Unique, randomly generated, Unicode, UTF\-8 encoded strings that are at most 1,024 bytes long\. Version Ids cannot be edited\.