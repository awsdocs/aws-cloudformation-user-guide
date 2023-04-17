# AWS::QuickSight::Template ColumnSort<a name="aws-properties-quicksight-template-columnsort"></a>

The sort configuration for a column that is not used in a field well\.

## Syntax<a name="aws-properties-quicksight-template-columnsort-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-columnsort-syntax.json"></a>

```
{
  "[AggregationFunction](#cfn-quicksight-template-columnsort-aggregationfunction)" : AggregationFunction,
  "[Direction](#cfn-quicksight-template-columnsort-direction)" : String,
  "[SortBy](#cfn-quicksight-template-columnsort-sortby)" : ColumnIdentifier
}
```

### YAML<a name="aws-properties-quicksight-template-columnsort-syntax.yaml"></a>

```
  [AggregationFunction](#cfn-quicksight-template-columnsort-aggregationfunction): 
    AggregationFunction
  [Direction](#cfn-quicksight-template-columnsort-direction): String
  [SortBy](#cfn-quicksight-template-columnsort-sortby): 
    ColumnIdentifier
```

## Properties<a name="aws-properties-quicksight-template-columnsort-properties"></a>

`AggregationFunction`  <a name="cfn-quicksight-template-columnsort-aggregationfunction"></a>
The aggregation function that is defined in the column sort\.  
*Required*: No  
*Type*: [AggregationFunction](aws-properties-quicksight-template-aggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Direction`  <a name="cfn-quicksight-template-columnsort-direction"></a>
The sort direction\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ASC | DESC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortBy`  <a name="cfn-quicksight-template-columnsort-sortby"></a>
Property description not available\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)