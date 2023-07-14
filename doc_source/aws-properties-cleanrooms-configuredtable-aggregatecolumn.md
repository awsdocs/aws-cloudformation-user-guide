# AWS::CleanRooms::ConfiguredTable AggregateColumn<a name="aws-properties-cleanrooms-configuredtable-aggregatecolumn"></a>

Column in configured table that can be used in aggregate function in query\.

## Syntax<a name="aws-properties-cleanrooms-configuredtable-aggregatecolumn-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cleanrooms-configuredtable-aggregatecolumn-syntax.json"></a>

```
{
  "[ColumnNames](#cfn-cleanrooms-configuredtable-aggregatecolumn-columnnames)" : [ String, ... ],
  "[Function](#cfn-cleanrooms-configuredtable-aggregatecolumn-function)" : String
}
```

### YAML<a name="aws-properties-cleanrooms-configuredtable-aggregatecolumn-syntax.yaml"></a>

```
  [ColumnNames](#cfn-cleanrooms-configuredtable-aggregatecolumn-columnnames): 
    - String
  [Function](#cfn-cleanrooms-configuredtable-aggregatecolumn-function): String
```

## Properties<a name="aws-properties-cleanrooms-configuredtable-aggregatecolumn-properties"></a>

`ColumnNames`  <a name="cfn-cleanrooms-configuredtable-aggregatecolumn-columnnames"></a>
Column names in configured table of aggregate columns\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Function`  <a name="cfn-cleanrooms-configuredtable-aggregatecolumn-function"></a>
Aggregation function that can be applied to aggregate column in query\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `AVG | COUNT | COUNT_DISTINCT | SUM | SUM_DISTINCT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)