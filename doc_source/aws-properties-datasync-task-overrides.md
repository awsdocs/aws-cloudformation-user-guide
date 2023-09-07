# AWS::DataSync::Task Overrides<a name="aws-properties-datasync-task-overrides"></a>

Customizes the reporting level for aspects of your task report\. For example, your report might generally only include errors, but you could specify that you want a list of successes and errors just for the files that DataSync attempted to delete in your destination location\.

## Syntax<a name="aws-properties-datasync-task-overrides-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-task-overrides-syntax.json"></a>

```
{
  "[Deleted](#cfn-datasync-task-overrides-deleted)" : Deleted,
  "[Skipped](#cfn-datasync-task-overrides-skipped)" : Skipped,
  "[Transferred](#cfn-datasync-task-overrides-transferred)" : Transferred,
  "[Verified](#cfn-datasync-task-overrides-verified)" : Verified
}
```

### YAML<a name="aws-properties-datasync-task-overrides-syntax.yaml"></a>

```
  [Deleted](#cfn-datasync-task-overrides-deleted): 
    Deleted
  [Skipped](#cfn-datasync-task-overrides-skipped): 
    Skipped
  [Transferred](#cfn-datasync-task-overrides-transferred): 
    Transferred
  [Verified](#cfn-datasync-task-overrides-verified): 
    Verified
```

## Properties<a name="aws-properties-datasync-task-overrides-properties"></a>

`Deleted`  <a name="cfn-datasync-task-overrides-deleted"></a>
Specifies the level of reporting for the files, objects, and directories that DataSync attempted to delete in your destination location\. This only applies if you [configure your task](https://docs.aws.amazon.com/datasync/latest/userguide/configure-metadata.html) to delete data in the destination that isn't in the source\.  
*Required*: No  
*Type*: [Deleted](aws-properties-datasync-task-deleted.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Skipped`  <a name="cfn-datasync-task-overrides-skipped"></a>
Specifies the level of reporting for the files, objects, and directories that DataSync attempted to skip during your transfer\.  
*Required*: No  
*Type*: [Skipped](aws-properties-datasync-task-skipped.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Transferred`  <a name="cfn-datasync-task-overrides-transferred"></a>
Specifies the level of reporting for the files, objects, and directories that DataSync attempted to transfer\.  
*Required*: No  
*Type*: [Transferred](aws-properties-datasync-task-transferred.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Verified`  <a name="cfn-datasync-task-overrides-verified"></a>
Specifies the level of reporting for the files, objects, and directories that DataSync attempted to verify during your transfer\.  
*Required*: No  
*Type*: [Verified](aws-properties-datasync-task-verified.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)