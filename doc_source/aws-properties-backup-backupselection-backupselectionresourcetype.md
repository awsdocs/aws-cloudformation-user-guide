# AWS::Backup::BackupSelection BackupSelectionResourceType<a name="aws-properties-backup-backupselection-backupselectionresourcetype"></a>

Specifies an object containing properties used to assign a set of resources to a backup plan\.

## Syntax<a name="aws-properties-backup-backupselection-backupselectionresourcetype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-backup-backupselection-backupselectionresourcetype-syntax.json"></a>

```
{
  "[Conditions](#cfn-backup-backupselection-backupselectionresourcetype-conditions)" : Conditions,
  "[IamRoleArn](#cfn-backup-backupselection-backupselectionresourcetype-iamrolearn)" : String,
  "[ListOfTags](#cfn-backup-backupselection-backupselectionresourcetype-listoftags)" : [ ConditionResourceType, ... ],
  "[NotResources](#cfn-backup-backupselection-backupselectionresourcetype-notresources)" : [ String, ... ],
  "[Resources](#cfn-backup-backupselection-backupselectionresourcetype-resources)" : [ String, ... ],
  "[SelectionName](#cfn-backup-backupselection-backupselectionresourcetype-selectionname)" : String
}
```

### YAML<a name="aws-properties-backup-backupselection-backupselectionresourcetype-syntax.yaml"></a>

```
  [Conditions](#cfn-backup-backupselection-backupselectionresourcetype-conditions): 
    Conditions
  [IamRoleArn](#cfn-backup-backupselection-backupselectionresourcetype-iamrolearn): String
  [ListOfTags](#cfn-backup-backupselection-backupselectionresourcetype-listoftags): 
    - ConditionResourceType
  [NotResources](#cfn-backup-backupselection-backupselectionresourcetype-notresources): 
    - String
  [Resources](#cfn-backup-backupselection-backupselectionresourcetype-resources): 
    - String
  [SelectionName](#cfn-backup-backupselection-backupselectionresourcetype-selectionname): String
```

## Properties<a name="aws-properties-backup-backupselection-backupselectionresourcetype-properties"></a>

`Conditions`  <a name="cfn-backup-backupselection-backupselectionresourcetype-conditions"></a>
A list of conditions that you define to assign resources to your backup plans using tags\. For example, `"StringEquals": { "ConditionKey": "aws:ResourceTag/CreatedByCryo", "ConditionValue": "true" },`\. Condition operators are case sensitive\.  
`Conditions` differs from `ListOfTags` as follows:  
+ When you specify more than one condition, you only assign the resources that match ALL conditions \(using AND logic\)\.
+ `Conditions` supports `StringEquals`, `StringLike`, `StringNotEquals`, and `StringNotLike`\. `ListOfTags` only supports `StringEquals`\.
*Required*: No  
*Type*: [Conditions](aws-properties-backup-backupselection-conditions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IamRoleArn`  <a name="cfn-backup-backupselection-backupselectionresourcetype-iamrolearn"></a>
The ARN of the IAM role that AWS Backup uses to authenticate when backing up the target resource; for example, `arn:aws:iam::123456789012:role/S3Access`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ListOfTags`  <a name="cfn-backup-backupselection-backupselectionresourcetype-listoftags"></a>
A list of conditions that you define to assign resources to your backup plans using tags\. For example, `"StringEquals": { "ConditionKey": "aws:ResourceTag/CreatedByCryo", "ConditionValue": "true" },`\. Condition operators are case sensitive\.  
`ListOfTags` differs from `Conditions` as follows:  
+ When you specify more than one condition, you assign all resources that match AT LEAST ONE condition \(using OR logic\)\.
+ `ListOfTags` only supports `StringEquals`\. `Conditions` supports `StringEquals`, `StringLike`, `StringNotEquals`, and `StringNotLike`\. 
*Required*: No  
*Type*: List of [ConditionResourceType](aws-properties-backup-backupselection-conditionresourcetype.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NotResources`  <a name="cfn-backup-backupselection-backupselectionresourcetype-notresources"></a>
A list of Amazon Resource Names \(ARNs\) to exclude from a backup plan\. The maximum number of ARNs is 500 without wildcards, or 30 ARNs with wildcards\.  
If you need to exclude many resources from a backup plan, consider a different resource selection strategy, such as assigning only one or a few resource types or refining your resource selection using tags\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Resources`  <a name="cfn-backup-backupselection-backupselectionresourcetype-resources"></a>
An array of strings that contain Amazon Resource Names \(ARNs\) of resources to assign to a backup plan\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SelectionName`  <a name="cfn-backup-backupselection-backupselectionresourcetype-selectionname"></a>
The display name of a resource selection document\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)