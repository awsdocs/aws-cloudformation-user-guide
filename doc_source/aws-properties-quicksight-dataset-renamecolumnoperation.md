# AWS::QuickSight::DataSet RenameColumnOperation<a name="aws-properties-quicksight-dataset-renamecolumnoperation"></a>

A transform operation that renames a column\.

## Syntax<a name="aws-properties-quicksight-dataset-renamecolumnoperation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-renamecolumnoperation-syntax.json"></a>

```
{
  "[ColumnName](#cfn-quicksight-dataset-renamecolumnoperation-columnname)" : String,
  "[NewColumnName](#cfn-quicksight-dataset-renamecolumnoperation-newcolumnname)" : String
}
```

### YAML<a name="aws-properties-quicksight-dataset-renamecolumnoperation-syntax.yaml"></a>

```
  [ColumnName](#cfn-quicksight-dataset-renamecolumnoperation-columnname): String
  [NewColumnName](#cfn-quicksight-dataset-renamecolumnoperation-newcolumnname): String
```

## Properties<a name="aws-properties-quicksight-dataset-renamecolumnoperation-properties"></a>

`ColumnName`  <a name="cfn-quicksight-dataset-renamecolumnoperation-columnname"></a>
The name of the column to be renamed\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NewColumnName`  <a name="cfn-quicksight-dataset-renamecolumnoperation-newcolumnname"></a>
The new name for the column\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)