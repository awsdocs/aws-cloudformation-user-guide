# AWS::QuickSight::Template DynamicDefaultValue<a name="aws-properties-quicksight-template-dynamicdefaultvalue"></a>

Defines different defaults to the users or groups based on mapping\.

## Syntax<a name="aws-properties-quicksight-template-dynamicdefaultvalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-dynamicdefaultvalue-syntax.json"></a>

```
{
  "[DefaultValueColumn](#cfn-quicksight-template-dynamicdefaultvalue-defaultvaluecolumn)" : ColumnIdentifier,
  "[GroupNameColumn](#cfn-quicksight-template-dynamicdefaultvalue-groupnamecolumn)" : ColumnIdentifier,
  "[UserNameColumn](#cfn-quicksight-template-dynamicdefaultvalue-usernamecolumn)" : ColumnIdentifier
}
```

### YAML<a name="aws-properties-quicksight-template-dynamicdefaultvalue-syntax.yaml"></a>

```
  [DefaultValueColumn](#cfn-quicksight-template-dynamicdefaultvalue-defaultvaluecolumn): 
    ColumnIdentifier
  [GroupNameColumn](#cfn-quicksight-template-dynamicdefaultvalue-groupnamecolumn): 
    ColumnIdentifier
  [UserNameColumn](#cfn-quicksight-template-dynamicdefaultvalue-usernamecolumn): 
    ColumnIdentifier
```

## Properties<a name="aws-properties-quicksight-template-dynamicdefaultvalue-properties"></a>

`DefaultValueColumn`  <a name="cfn-quicksight-template-dynamicdefaultvalue-defaultvaluecolumn"></a>
The column that contains the default value of each user or group\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupNameColumn`  <a name="cfn-quicksight-template-dynamicdefaultvalue-groupnamecolumn"></a>
The column that contains the group name\.  
*Required*: No  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserNameColumn`  <a name="cfn-quicksight-template-dynamicdefaultvalue-usernamecolumn"></a>
The column that contains the username\.  
*Required*: No  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)