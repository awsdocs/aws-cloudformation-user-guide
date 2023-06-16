# AWS::CleanRooms::ConfiguredTable AggregationConstraint<a name="aws-properties-cleanrooms-configuredtable-aggregationconstraint"></a>

Constraint on query output removing output rows that do not meet a minimum number of distinct values of a specified column\.

## Syntax<a name="aws-properties-cleanrooms-configuredtable-aggregationconstraint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cleanrooms-configuredtable-aggregationconstraint-syntax.json"></a>

```
{
  "[ColumnName](#cfn-cleanrooms-configuredtable-aggregationconstraint-columnname)" : String,
  "[Minimum](#cfn-cleanrooms-configuredtable-aggregationconstraint-minimum)" : Double,
  "[Type](#cfn-cleanrooms-configuredtable-aggregationconstraint-type)" : String
}
```

### YAML<a name="aws-properties-cleanrooms-configuredtable-aggregationconstraint-syntax.yaml"></a>

```
  [ColumnName](#cfn-cleanrooms-configuredtable-aggregationconstraint-columnname): String
  [Minimum](#cfn-cleanrooms-configuredtable-aggregationconstraint-minimum): Double
  [Type](#cfn-cleanrooms-configuredtable-aggregationconstraint-type): String
```

## Properties<a name="aws-properties-cleanrooms-configuredtable-aggregationconstraint-properties"></a>

`ColumnName`  <a name="cfn-cleanrooms-configuredtable-aggregationconstraint-columnname"></a>
Column in aggregation constraint for which there must be a minimum number of distinct values in an output row for it to be in the query output\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `127`  
*Pattern*: `[a-z0-9_](([a-z0-9_ ]+-)*([a-z0-9_ ]+))?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Minimum`  <a name="cfn-cleanrooms-configuredtable-aggregationconstraint-minimum"></a>
The minimum number of distinct values that an output row must be an aggregation of\. Minimum threshold of distinct values for a specified column that must exist in an output row for it to be in the query output\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `2`  
*Maximum*: `100000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-cleanrooms-configuredtable-aggregationconstraint-type"></a>
The type of aggregation the constraint allows\. The only valid value is currently `COUNT\_DISTINCT`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `COUNT_DISTINCT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)