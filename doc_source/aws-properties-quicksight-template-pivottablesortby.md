# AWS::QuickSight::Template PivotTableSortBy<a name="aws-properties-quicksight-template-pivottablesortby"></a>

The sort by field for the field sort options\.

## Syntax<a name="aws-properties-quicksight-template-pivottablesortby-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-pivottablesortby-syntax.json"></a>

```
{
  "[Column](#cfn-quicksight-template-pivottablesortby-column)" : ColumnSort,
  "[DataPath](#cfn-quicksight-template-pivottablesortby-datapath)" : DataPathSort,
  "[Field](#cfn-quicksight-template-pivottablesortby-field)" : FieldSort
}
```

### YAML<a name="aws-properties-quicksight-template-pivottablesortby-syntax.yaml"></a>

```
  [Column](#cfn-quicksight-template-pivottablesortby-column): 
    ColumnSort
  [DataPath](#cfn-quicksight-template-pivottablesortby-datapath): 
    DataPathSort
  [Field](#cfn-quicksight-template-pivottablesortby-field): 
    FieldSort
```

## Properties<a name="aws-properties-quicksight-template-pivottablesortby-properties"></a>

`Column`  <a name="cfn-quicksight-template-pivottablesortby-column"></a>
The column sort \(field id, direction\) for the pivot table sort by options\.  
*Required*: No  
*Type*: [ColumnSort](aws-properties-quicksight-template-columnsort.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataPath`  <a name="cfn-quicksight-template-pivottablesortby-datapath"></a>
The data path sort \(data path value, direction\) for the pivot table sort by options\.  
*Required*: No  
*Type*: [DataPathSort](aws-properties-quicksight-template-datapathsort.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Field`  <a name="cfn-quicksight-template-pivottablesortby-field"></a>
The field sort \(field id, direction\) for the pivot table sort by options\.  
*Required*: No  
*Type*: [FieldSort](aws-properties-quicksight-template-fieldsort.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)