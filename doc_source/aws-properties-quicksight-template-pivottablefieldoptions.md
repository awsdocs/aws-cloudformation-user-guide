# AWS::QuickSight::Template PivotTableFieldOptions<a name="aws-properties-quicksight-template-pivottablefieldoptions"></a>

The field options for a pivot table visual\.

## Syntax<a name="aws-properties-quicksight-template-pivottablefieldoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-pivottablefieldoptions-syntax.json"></a>

```
{
  "[CollapseStateOptions](#cfn-quicksight-template-pivottablefieldoptions-collapsestateoptions)" : [ PivotTableFieldCollapseStateOption, ... ],
  "[DataPathOptions](#cfn-quicksight-template-pivottablefieldoptions-datapathoptions)" : [ PivotTableDataPathOption, ... ],
  "[SelectedFieldOptions](#cfn-quicksight-template-pivottablefieldoptions-selectedfieldoptions)" : [ PivotTableFieldOption, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-pivottablefieldoptions-syntax.yaml"></a>

```
  [CollapseStateOptions](#cfn-quicksight-template-pivottablefieldoptions-collapsestateoptions): 
    - PivotTableFieldCollapseStateOption
  [DataPathOptions](#cfn-quicksight-template-pivottablefieldoptions-datapathoptions): 
    - PivotTableDataPathOption
  [SelectedFieldOptions](#cfn-quicksight-template-pivottablefieldoptions-selectedfieldoptions): 
    - PivotTableFieldOption
```

## Properties<a name="aws-properties-quicksight-template-pivottablefieldoptions-properties"></a>

`CollapseStateOptions`  <a name="cfn-quicksight-template-pivottablefieldoptions-collapsestateoptions"></a>
The collapse state options for the pivot table field options\.  
*Required*: No  
*Type*: List of [PivotTableFieldCollapseStateOption](aws-properties-quicksight-template-pivottablefieldcollapsestateoption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataPathOptions`  <a name="cfn-quicksight-template-pivottablefieldoptions-datapathoptions"></a>
The data path options for the pivot table field options\.  
*Required*: No  
*Type*: List of [PivotTableDataPathOption](aws-properties-quicksight-template-pivottabledatapathoption.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectedFieldOptions`  <a name="cfn-quicksight-template-pivottablefieldoptions-selectedfieldoptions"></a>
The selected field options for the pivot table field options\.  
*Required*: No  
*Type*: List of [PivotTableFieldOption](aws-properties-quicksight-template-pivottablefieldoption.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)