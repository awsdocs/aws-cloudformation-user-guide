# AWS::Backup::BackupSelection<a name="aws-resource-backup-backupselection"></a>

Specifies a set of resources to assign to a backup plan\.

## Syntax<a name="aws-resource-backup-backupselection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-backup-backupselection-syntax.json"></a>

```
{
  "Type" : "AWS::Backup::BackupSelection",
  "Properties" : {
      "[BackupPlanId](#cfn-backup-backupselection-backupplanid)" : String,
      "[BackupSelection](#cfn-backup-backupselection-backupselection)" : BackupSelectionResourceType
    }
}
```

### YAML<a name="aws-resource-backup-backupselection-syntax.yaml"></a>

```
Type: AWS::Backup::BackupSelection
Properties: 
  [BackupPlanId](#cfn-backup-backupselection-backupplanid): String
  [BackupSelection](#cfn-backup-backupselection-backupselection): 
    BackupSelectionResourceType
```

## Properties<a name="aws-resource-backup-backupselection-properties"></a>

`BackupPlanId`  <a name="cfn-backup-backupselection-backupplanid"></a>
Uniquely identifies a backup plan\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BackupSelection`  <a name="cfn-backup-backupselection-backupselection"></a>
Specifies the body of a request to assign a set of resources to a backup plan\.  
It includes an array of resources, an optional array of patterns to exclude resources, an optional role to provide access to the AWS service the resource belongs to, and an optional array of tags used to identify a set of resources\.  
*Required*: Yes  
*Type*: [BackupSelectionResourceType](aws-properties-backup-backupselection-backupselectionresourcetype.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-backup-backupselection-return-values"></a>

### Ref<a name="aws-resource-backup-backupselection-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns `BackupSelectionId`\.

### Fn::GetAtt<a name="aws-resource-backup-backupselection-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-backup-backupselection-return-values-fn--getatt-fn--getatt"></a>

`BackupPlanId`  <a name="BackupPlanId-fn::getatt"></a>
Uniquely identifies a backup plan\.

`SelectionId`  <a name="SelectionId-fn::getatt"></a>
Uniquely identifies a request to assign a set of resources to a backup plan\.