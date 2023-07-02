# AWS::QuickSight::Template AggregationSortConfiguration<a name="aws-properties-quicksight-template-aggregationsortconfiguration"></a>

The configuration options to sort aggregated values\.

## Syntax<a name="aws-properties-quicksight-template-aggregationsortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-aggregationsortconfiguration-syntax.json"></a>

```
{
  "[AggregationFunction](#cfn-quicksight-template-aggregationsortconfiguration-aggregationfunction)" : AggregationFunction,
  "[Column](#cfn-quicksight-template-aggregationsortconfiguration-column)" : ColumnIdentifier,
  "[SortDirection](#cfn-quicksight-template-aggregationsortconfiguration-sortdirection)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-aggregationsortconfiguration-syntax.yaml"></a>

```
  [AggregationFunction](#cfn-quicksight-template-aggregationsortconfiguration-aggregationfunction): 
    AggregationFunction
  [Column](#cfn-quicksight-template-aggregationsortconfiguration-column): 
    ColumnIdentifier
  [SortDirection](#cfn-quicksight-template-aggregationsortconfiguration-sortdirection): String
```

## Properties<a name="aws-properties-quicksight-template-aggregationsortconfiguration-properties"></a>

`AggregationFunction`  <a name="cfn-quicksight-template-aggregationsortconfiguration-aggregationfunction"></a>
The function that aggregates the values in `Column`\.  
*Required*: No  
*Type*: [AggregationFunction](aws-properties-quicksight-template-aggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Column`  <a name="cfn-quicksight-template-aggregationsortconfiguration-column"></a>
The column that determines the sort order of aggregated values\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortDirection`  <a name="cfn-quicksight-template-aggregationsortconfiguration-sortdirection"></a>
The sort direction of values\.  
+  `ASC`: Sort in ascending order\.
+  `DESC`: Sort in descending order\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `ASC | DESC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)