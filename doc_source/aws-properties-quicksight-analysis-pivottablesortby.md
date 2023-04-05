# AWS::QuickSight::Analysis PivotTableSortBy<a name="aws-properties-quicksight-analysis-pivottablesortby"></a>

The sort by field for the field sort options\.

## Syntax<a name="aws-properties-quicksight-analysis-pivottablesortby-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-pivottablesortby-syntax.json"></a>

```
{
  "[Column](#cfn-quicksight-analysis-pivottablesortby-column)" : ColumnSort,
  "[DataPath](#cfn-quicksight-analysis-pivottablesortby-datapath)" : DataPathSort,
  "[Field](#cfn-quicksight-analysis-pivottablesortby-field)" : FieldSort
}
```

### YAML<a name="aws-properties-quicksight-analysis-pivottablesortby-syntax.yaml"></a>

```
  [Column](#cfn-quicksight-analysis-pivottablesortby-column): 
    ColumnSort
  [DataPath](#cfn-quicksight-analysis-pivottablesortby-datapath): 
    DataPathSort
  [Field](#cfn-quicksight-analysis-pivottablesortby-field): 
    FieldSort
```

## Properties<a name="aws-properties-quicksight-analysis-pivottablesortby-properties"></a>

`Column`  <a name="cfn-quicksight-analysis-pivottablesortby-column"></a>
The column sort \(field id, direction\) for the pivot table sort by options\.  
*Required*: No  
*Type*: [ColumnSort](aws-properties-quicksight-analysis-columnsort.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataPath`  <a name="cfn-quicksight-analysis-pivottablesortby-datapath"></a>
The data path sort \(data path value, direction\) for the pivot table sort by options\.  
*Required*: No  
*Type*: [DataPathSort](aws-properties-quicksight-analysis-datapathsort.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Field`  <a name="cfn-quicksight-analysis-pivottablesortby-field"></a>
The field sort \(field id, direction\) for the pivot table sort by options\.  
*Required*: No  
*Type*: [FieldSort](aws-properties-quicksight-analysis-fieldsort.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)