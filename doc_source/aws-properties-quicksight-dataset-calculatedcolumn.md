# AWS::QuickSight::DataSet CalculatedColumn<a name="aws-properties-quicksight-dataset-calculatedcolumn"></a>

A calculated column for a dataset\.

## Syntax<a name="aws-properties-quicksight-dataset-calculatedcolumn-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-calculatedcolumn-syntax.json"></a>

```
{
  "[ColumnId](#cfn-quicksight-dataset-calculatedcolumn-columnid)" : String,
  "[ColumnName](#cfn-quicksight-dataset-calculatedcolumn-columnname)" : String,
  "[Expression](#cfn-quicksight-dataset-calculatedcolumn-expression)" : String
}
```

### YAML<a name="aws-properties-quicksight-dataset-calculatedcolumn-syntax.yaml"></a>

```
  [ColumnId](#cfn-quicksight-dataset-calculatedcolumn-columnid): String
  [ColumnName](#cfn-quicksight-dataset-calculatedcolumn-columnname): String
  [Expression](#cfn-quicksight-dataset-calculatedcolumn-expression): String
```

## Properties<a name="aws-properties-quicksight-dataset-calculatedcolumn-properties"></a>

`ColumnId`  <a name="cfn-quicksight-dataset-calculatedcolumn-columnid"></a>
A unique ID to identify a calculated column\. During a dataset update, if the column ID of a calculated column matches that of an existing calculated column, Amazon QuickSight preserves the existing calculated column\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnName`  <a name="cfn-quicksight-dataset-calculatedcolumn-columnname"></a>
Column name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expression`  <a name="cfn-quicksight-dataset-calculatedcolumn-expression"></a>
An expression that defines the calculated column\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)