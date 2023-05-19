# AWS::QuickSight::Topic DataAggregation<a name="aws-properties-quicksight-topic-dataaggregation"></a>

The definition of a data aggregation\.

## Syntax<a name="aws-properties-quicksight-topic-dataaggregation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-dataaggregation-syntax.json"></a>

```
{
  "[DatasetRowDateGranularity](#cfn-quicksight-topic-dataaggregation-datasetrowdategranularity)" : String,
  "[DefaultDateColumnName](#cfn-quicksight-topic-dataaggregation-defaultdatecolumnname)" : String
}
```

### YAML<a name="aws-properties-quicksight-topic-dataaggregation-syntax.yaml"></a>

```
  [DatasetRowDateGranularity](#cfn-quicksight-topic-dataaggregation-datasetrowdategranularity): String
  [DefaultDateColumnName](#cfn-quicksight-topic-dataaggregation-defaultdatecolumnname): String
```

## Properties<a name="aws-properties-quicksight-topic-dataaggregation-properties"></a>

`DatasetRowDateGranularity`  <a name="cfn-quicksight-topic-dataaggregation-datasetrowdategranularity"></a>
The level of time precision that is used to aggregate `DateTime` values\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DAY | HOUR | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultDateColumnName`  <a name="cfn-quicksight-topic-dataaggregation-defaultdatecolumnname"></a>
The column name for the default date\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)