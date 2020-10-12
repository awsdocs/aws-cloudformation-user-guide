# AWS::Backup::BackupSelection ConditionResourceType<a name="aws-properties-backup-backupselection-conditionresourcetype"></a>

Specifies an object that contains an array of triplets made up of a condition type \(such as `StringEquals`\), a key, and a value\. Conditions are used to filter resources in a selection that is assigned to a backup plan\.

## Syntax<a name="aws-properties-backup-backupselection-conditionresourcetype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-backup-backupselection-conditionresourcetype-syntax.json"></a>

```
{
  "[ConditionKey](#cfn-backup-backupselection-conditionresourcetype-conditionkey)" : String,
  "[ConditionType](#cfn-backup-backupselection-conditionresourcetype-conditiontype)" : String,
  "[ConditionValue](#cfn-backup-backupselection-conditionresourcetype-conditionvalue)" : String
}
```

### YAML<a name="aws-properties-backup-backupselection-conditionresourcetype-syntax.yaml"></a>

```
  [ConditionKey](#cfn-backup-backupselection-conditionresourcetype-conditionkey): String
  [ConditionType](#cfn-backup-backupselection-conditionresourcetype-conditiontype): String
  [ConditionValue](#cfn-backup-backupselection-conditionresourcetype-conditionvalue): String
```

## Properties<a name="aws-properties-backup-backupselection-conditionresourcetype-properties"></a>

`ConditionKey`  <a name="cfn-backup-backupselection-conditionresourcetype-conditionkey"></a>
The key in a key\-value pair\. For example, in `"ec2:ResourceTag/Department": "accounting"`, `"ec2:ResourceTag/Department"` is the key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConditionType`  <a name="cfn-backup-backupselection-conditionresourcetype-conditiontype"></a>
An operation, such as `StringEquals`, that is applied to a key\-value pair used to filter resources in a selection\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConditionValue`  <a name="cfn-backup-backupselection-conditionresourcetype-conditionvalue"></a>
The value in a key\-value pair\. For example, in `"ec2:ResourceTag/Department": "accounting"`, `"accounting"` is the value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)