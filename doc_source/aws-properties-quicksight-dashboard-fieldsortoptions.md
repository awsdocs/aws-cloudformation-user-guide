# AWS::QuickSight::Dashboard FieldSortOptions<a name="aws-properties-quicksight-dashboard-fieldsortoptions"></a>

The field sort options in a chart configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-fieldsortoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-fieldsortoptions-syntax.json"></a>

```
{
  "[ColumnSort](#cfn-quicksight-dashboard-fieldsortoptions-columnsort)" : ColumnSort,
  "[FieldSort](#cfn-quicksight-dashboard-fieldsortoptions-fieldsort)" : FieldSort
}
```

### YAML<a name="aws-properties-quicksight-dashboard-fieldsortoptions-syntax.yaml"></a>

```
  [ColumnSort](#cfn-quicksight-dashboard-fieldsortoptions-columnsort): 
    ColumnSort
  [FieldSort](#cfn-quicksight-dashboard-fieldsortoptions-fieldsort): 
    FieldSort
```

## Properties<a name="aws-properties-quicksight-dashboard-fieldsortoptions-properties"></a>

`ColumnSort`  <a name="cfn-quicksight-dashboard-fieldsortoptions-columnsort"></a>
The sort configuration for a column that is not used in a field well\.  
*Required*: No  
*Type*: [ColumnSort](aws-properties-quicksight-dashboard-columnsort.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldSort`  <a name="cfn-quicksight-dashboard-fieldsortoptions-fieldsort"></a>
The sort configuration for a field in a field well\.  
*Required*: No  
*Type*: [FieldSort](aws-properties-quicksight-dashboard-fieldsort.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)