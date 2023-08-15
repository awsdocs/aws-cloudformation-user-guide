# AWS::QuickSight::Analysis TableFieldOptions<a name="aws-properties-quicksight-analysis-tablefieldoptions"></a>

The field options for a table visual\.

## Syntax<a name="aws-properties-quicksight-analysis-tablefieldoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-tablefieldoptions-syntax.json"></a>

```
{
  "[Order](#cfn-quicksight-analysis-tablefieldoptions-order)" : [ String, ... ],
  "[SelectedFieldOptions](#cfn-quicksight-analysis-tablefieldoptions-selectedfieldoptions)" : [ TableFieldOption, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-tablefieldoptions-syntax.yaml"></a>

```
  [Order](#cfn-quicksight-analysis-tablefieldoptions-order): 
    - String
  [SelectedFieldOptions](#cfn-quicksight-analysis-tablefieldoptions-selectedfieldoptions): 
    - TableFieldOption
```

## Properties<a name="aws-properties-quicksight-analysis-tablefieldoptions-properties"></a>

`Order`  <a name="cfn-quicksight-analysis-tablefieldoptions-order"></a>
The order of field IDs of the field options for a table visual\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectedFieldOptions`  <a name="cfn-quicksight-analysis-tablefieldoptions-selectedfieldoptions"></a>
The selected field options for the table field options\.  
*Required*: No  
*Type*: List of [TableFieldOption](aws-properties-quicksight-analysis-tablefieldoption.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)