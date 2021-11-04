# AWS::QuickSight::Theme ResourcePermission<a name="aws-properties-quicksight-theme-resourcepermission"></a>

Permission for the resource\.

## Syntax<a name="aws-properties-quicksight-theme-resourcepermission-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-theme-resourcepermission-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-theme-resourcepermission-actions)" : [ String, ... ],
  "[Principal](#cfn-quicksight-theme-resourcepermission-principal)" : String
}
```

### YAML<a name="aws-properties-quicksight-theme-resourcepermission-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-theme-resourcepermission-actions): 
    - String
  [Principal](#cfn-quicksight-theme-resourcepermission-principal): String
```

## Properties<a name="aws-properties-quicksight-theme-resourcepermission-properties"></a>

`Actions`  <a name="cfn-quicksight-theme-resourcepermission-actions"></a>
The IAM action to grant or revoke permissions on\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Principal`  <a name="cfn-quicksight-theme-resourcepermission-principal"></a>
The Amazon Resource Name \(ARN\) of the principal\. This can be one of the following:  
+ The ARN of an Amazon QuickSight user or group associated with a data source or dataset\. \(This is common\.\)
+ The ARN of an Amazon QuickSight user, group, or namespace associated with an analysis, dashboard, template, or theme\. \(This is common\.\)
+ The ARN of an AWS account root: This is an IAM ARN rather than a Amazon QuickSight ARN\. Use this option only to share resources \(templates\) across AWS accounts\. \(This is less common\.\)
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)