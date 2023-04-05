# AWS::QuickSight::Analysis FilterOperationSelectedFieldsConfiguration<a name="aws-properties-quicksight-analysis-filteroperationselectedfieldsconfiguration"></a>

The configuration of selected fields in the`CustomActionFilterOperation`\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-filteroperationselectedfieldsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-filteroperationselectedfieldsconfiguration-syntax.json"></a>

```
{
  "[SelectedFieldOptions](#cfn-quicksight-analysis-filteroperationselectedfieldsconfiguration-selectedfieldoptions)" : String,
  "[SelectedFields](#cfn-quicksight-analysis-filteroperationselectedfieldsconfiguration-selectedfields)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-filteroperationselectedfieldsconfiguration-syntax.yaml"></a>

```
  [SelectedFieldOptions](#cfn-quicksight-analysis-filteroperationselectedfieldsconfiguration-selectedfieldoptions): String
  [SelectedFields](#cfn-quicksight-analysis-filteroperationselectedfieldsconfiguration-selectedfields): 
    - String
```

## Properties<a name="aws-properties-quicksight-analysis-filteroperationselectedfieldsconfiguration-properties"></a>

`SelectedFieldOptions`  <a name="cfn-quicksight-analysis-filteroperationselectedfieldsconfiguration-selectedfieldoptions"></a>
A structure that contains the options that choose which fields are filtered in the `CustomActionFilterOperation`\.  
Valid values are defined as follows:  
+  `ALL_FIELDS`: Applies the filter operation to all fields\.
*Required*: No  
*Type*: String  
*Allowed values*: `ALL_FIELDS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectedFields`  <a name="cfn-quicksight-analysis-filteroperationselectedfieldsconfiguration-selectedfields"></a>
Chooses the fields that are filtered in `CustomActionFilterOperation`\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)