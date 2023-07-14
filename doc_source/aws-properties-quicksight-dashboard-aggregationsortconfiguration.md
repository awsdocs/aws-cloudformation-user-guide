# AWS::QuickSight::Dashboard AggregationSortConfiguration<a name="aws-properties-quicksight-dashboard-aggregationsortconfiguration"></a>

The configuration options to sort aggregated values\.

## Syntax<a name="aws-properties-quicksight-dashboard-aggregationsortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-aggregationsortconfiguration-syntax.json"></a>

```
{
  "[AggregationFunction](#cfn-quicksight-dashboard-aggregationsortconfiguration-aggregationfunction)" : AggregationFunction,
  "[Column](#cfn-quicksight-dashboard-aggregationsortconfiguration-column)" : ColumnIdentifier,
  "[SortDirection](#cfn-quicksight-dashboard-aggregationsortconfiguration-sortdirection)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-aggregationsortconfiguration-syntax.yaml"></a>

```
  [AggregationFunction](#cfn-quicksight-dashboard-aggregationsortconfiguration-aggregationfunction): 
    AggregationFunction
  [Column](#cfn-quicksight-dashboard-aggregationsortconfiguration-column): 
    ColumnIdentifier
  [SortDirection](#cfn-quicksight-dashboard-aggregationsortconfiguration-sortdirection): String
```

## Properties<a name="aws-properties-quicksight-dashboard-aggregationsortconfiguration-properties"></a>

`AggregationFunction`  <a name="cfn-quicksight-dashboard-aggregationsortconfiguration-aggregationfunction"></a>
The function that aggregates the values in `Column`\.  
*Required*: No  
*Type*: [AggregationFunction](aws-properties-quicksight-dashboard-aggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Column`  <a name="cfn-quicksight-dashboard-aggregationsortconfiguration-column"></a>
The column that determines the sort order of aggregated values\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-dashboard-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortDirection`  <a name="cfn-quicksight-dashboard-aggregationsortconfiguration-sortdirection"></a>
The sort direction of values\.  
+  `ASC`: Sort in ascending order\.
+  `DESC`: Sort in descending order\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `ASC | DESC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)