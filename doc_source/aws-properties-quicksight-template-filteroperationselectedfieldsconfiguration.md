# AWS::QuickSight::Template FilterOperationSelectedFieldsConfiguration<a name="aws-properties-quicksight-template-filteroperationselectedfieldsconfiguration"></a>

The configuration of selected fields in the`CustomActionFilterOperation`\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-filteroperationselectedfieldsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-filteroperationselectedfieldsconfiguration-syntax.json"></a>

```
{
  "[SelectedColumns](#cfn-quicksight-template-filteroperationselectedfieldsconfiguration-selectedcolumns)" : [ ColumnIdentifier, ... ],
  "[SelectedFieldOptions](#cfn-quicksight-template-filteroperationselectedfieldsconfiguration-selectedfieldoptions)" : String,
  "[SelectedFields](#cfn-quicksight-template-filteroperationselectedfieldsconfiguration-selectedfields)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-filteroperationselectedfieldsconfiguration-syntax.yaml"></a>

```
  [SelectedColumns](#cfn-quicksight-template-filteroperationselectedfieldsconfiguration-selectedcolumns): 
    - ColumnIdentifier
  [SelectedFieldOptions](#cfn-quicksight-template-filteroperationselectedfieldsconfiguration-selectedfieldoptions): String
  [SelectedFields](#cfn-quicksight-template-filteroperationselectedfieldsconfiguration-selectedfields): 
    - String
```

## Properties<a name="aws-properties-quicksight-template-filteroperationselectedfieldsconfiguration-properties"></a>

`SelectedColumns`  <a name="cfn-quicksight-template-filteroperationselectedfieldsconfiguration-selectedcolumns"></a>
The selected columns of a dataset\.  
*Required*: No  
*Type*: List of [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectedFieldOptions`  <a name="cfn-quicksight-template-filteroperationselectedfieldsconfiguration-selectedfieldoptions"></a>
A structure that contains the options that choose which fields are filtered in the `CustomActionFilterOperation`\.  
Valid values are defined as follows:  
+  `ALL_FIELDS`: Applies the filter operation to all fields\.
*Required*: No  
*Type*: String  
*Allowed values*: `ALL_FIELDS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectedFields`  <a name="cfn-quicksight-template-filteroperationselectedfieldsconfiguration-selectedfields"></a>
Chooses the fields that are filtered in `CustomActionFilterOperation`\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)