# AWS::QuickSight::Topic TopicNumericEqualityFilter<a name="aws-properties-quicksight-topic-topicnumericequalityfilter"></a>

A filter that filters topics based on the value of a numeric field\. The filter includes only topics whose numeric field value matches the specified value\.

## Syntax<a name="aws-properties-quicksight-topic-topicnumericequalityfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-topicnumericequalityfilter-syntax.json"></a>

```
{
  "[Aggregation](#cfn-quicksight-topic-topicnumericequalityfilter-aggregation)" : String,
  "[Constant](#cfn-quicksight-topic-topicnumericequalityfilter-constant)" : TopicSingularFilterConstant
}
```

### YAML<a name="aws-properties-quicksight-topic-topicnumericequalityfilter-syntax.yaml"></a>

```
  [Aggregation](#cfn-quicksight-topic-topicnumericequalityfilter-aggregation): String
  [Constant](#cfn-quicksight-topic-topicnumericequalityfilter-constant): 
    TopicSingularFilterConstant
```

## Properties<a name="aws-properties-quicksight-topic-topicnumericequalityfilter-properties"></a>

`Aggregation`  <a name="cfn-quicksight-topic-topicnumericequalityfilter-aggregation"></a>
An aggregation function that specifies how to calculate the value of a numeric field for a topic\. Valid values for this structure are `NO_AGGREGATION`, `SUM`, `AVERAGE`, `COUNT`, `DISTINCT_COUNT`, `MAX`, `MEDIAN`, `MIN`, `STDEV`, `STDEVP`, `VAR`, and `VARP`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AVERAGE | COUNT | DISTINCT_COUNT | MAX | MEDIAN | MIN | NO_AGGREGATION | STDEV | STDEVP | SUM | VAR | VARP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Constant`  <a name="cfn-quicksight-topic-topicnumericequalityfilter-constant"></a>
The constant used in a numeric equality filter\.  
*Required*: No  
*Type*: [TopicSingularFilterConstant](aws-properties-quicksight-topic-topicsingularfilterconstant.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)