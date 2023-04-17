# AWS::QuickSight::Analysis FieldSortOptions<a name="aws-properties-quicksight-analysis-fieldsortoptions"></a>

The field sort options in a chart configuration\.

## Syntax<a name="aws-properties-quicksight-analysis-fieldsortoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-fieldsortoptions-syntax.json"></a>

```
{
  "[ColumnSort](#cfn-quicksight-analysis-fieldsortoptions-columnsort)" : ColumnSort,
  "[FieldSort](#cfn-quicksight-analysis-fieldsortoptions-fieldsort)" : FieldSort
}
```

### YAML<a name="aws-properties-quicksight-analysis-fieldsortoptions-syntax.yaml"></a>

```
  [ColumnSort](#cfn-quicksight-analysis-fieldsortoptions-columnsort): 
    ColumnSort
  [FieldSort](#cfn-quicksight-analysis-fieldsortoptions-fieldsort): 
    FieldSort
```

## Properties<a name="aws-properties-quicksight-analysis-fieldsortoptions-properties"></a>

`ColumnSort`  <a name="cfn-quicksight-analysis-fieldsortoptions-columnsort"></a>
The sort configuration for a column that is not used in a field well\.  
*Required*: No  
*Type*: [ColumnSort](aws-properties-quicksight-analysis-columnsort.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldSort`  <a name="cfn-quicksight-analysis-fieldsortoptions-fieldsort"></a>
The sort configuration for a field in a field well\.  
*Required*: No  
*Type*: [FieldSort](aws-properties-quicksight-analysis-fieldsort.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)