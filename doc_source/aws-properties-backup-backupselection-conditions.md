# AWS::Backup::BackupSelection Conditions<a name="aws-properties-backup-backupselection-conditions"></a>

Contains information about which resources to include or exclude from a backup plan using their tags\. Conditions are case sensitive\.

## Syntax<a name="aws-properties-backup-backupselection-conditions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-backup-backupselection-conditions-syntax.json"></a>

```
{
  "[StringEquals](#cfn-backup-backupselection-conditions-stringequals)" : [ ConditionParameter, ... ],
  "[StringLike](#cfn-backup-backupselection-conditions-stringlike)" : [ ConditionParameter, ... ],
  "[StringNotEquals](#cfn-backup-backupselection-conditions-stringnotequals)" : [ ConditionParameter, ... ],
  "[StringNotLike](#cfn-backup-backupselection-conditions-stringnotlike)" : [ ConditionParameter, ... ]
}
```

### YAML<a name="aws-properties-backup-backupselection-conditions-syntax.yaml"></a>

```
  [StringEquals](#cfn-backup-backupselection-conditions-stringequals): 
    - ConditionParameter
  [StringLike](#cfn-backup-backupselection-conditions-stringlike): 
    - ConditionParameter
  [StringNotEquals](#cfn-backup-backupselection-conditions-stringnotequals): 
    - ConditionParameter
  [StringNotLike](#cfn-backup-backupselection-conditions-stringnotlike): 
    - ConditionParameter
```

## Properties<a name="aws-properties-backup-backupselection-conditions-properties"></a>

`StringEquals`  <a name="cfn-backup-backupselection-conditions-stringequals"></a>
Filters the values of your tagged resources for only those resources that you tagged with the same value\. Also called "exact matching\."  
*Required*: No  
*Type*: List of [ConditionParameter](aws-properties-backup-backupselection-conditionparameter.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StringLike`  <a name="cfn-backup-backupselection-conditions-stringlike"></a>
Filters the values of your tagged resources for matching tag values with the use of a wildcard character \(\*\) anywhere in the string\. For example, "prod\*" or "\*rod\*" matches the tag value "production"\.  
*Required*: No  
*Type*: List of [ConditionParameter](aws-properties-backup-backupselection-conditionparameter.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StringNotEquals`  <a name="cfn-backup-backupselection-conditions-stringnotequals"></a>
Filters the values of your tagged resources for only those resources that you tagged that do not have the same value\. Also called "negated matching\."  
*Required*: No  
*Type*: List of [ConditionParameter](aws-properties-backup-backupselection-conditionparameter.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StringNotLike`  <a name="cfn-backup-backupselection-conditions-stringnotlike"></a>
Filters the values of your tagged resources for non\-matching tag values with the use of a wildcard character \(\*\) anywhere in the string\.  
*Required*: No  
*Type*: List of [ConditionParameter](aws-properties-backup-backupselection-conditionparameter.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)