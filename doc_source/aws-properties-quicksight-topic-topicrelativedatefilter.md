# AWS::QuickSight::Topic TopicRelativeDateFilter<a name="aws-properties-quicksight-topic-topicrelativedatefilter"></a>

A structure that represents a relative date filter\.

## Syntax<a name="aws-properties-quicksight-topic-topicrelativedatefilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-topicrelativedatefilter-syntax.json"></a>

```
{
  "[Constant](#cfn-quicksight-topic-topicrelativedatefilter-constant)" : TopicSingularFilterConstant,
  "[RelativeDateFilterFunction](#cfn-quicksight-topic-topicrelativedatefilter-relativedatefilterfunction)" : String,
  "[TimeGranularity](#cfn-quicksight-topic-topicrelativedatefilter-timegranularity)" : String
}
```

### YAML<a name="aws-properties-quicksight-topic-topicrelativedatefilter-syntax.yaml"></a>

```
  [Constant](#cfn-quicksight-topic-topicrelativedatefilter-constant): 
    TopicSingularFilterConstant
  [RelativeDateFilterFunction](#cfn-quicksight-topic-topicrelativedatefilter-relativedatefilterfunction): String
  [TimeGranularity](#cfn-quicksight-topic-topicrelativedatefilter-timegranularity): String
```

## Properties<a name="aws-properties-quicksight-topic-topicrelativedatefilter-properties"></a>

`Constant`  <a name="cfn-quicksight-topic-topicrelativedatefilter-constant"></a>
The constant used in a relative date filter\.  
*Required*: No  
*Type*: [TopicSingularFilterConstant](aws-properties-quicksight-topic-topicsingularfilterconstant.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelativeDateFilterFunction`  <a name="cfn-quicksight-topic-topicrelativedatefilter-relativedatefilterfunction"></a>
The function to be used in a relative date filter to determine the range of dates to include in the results\. Valid values for this structure are `BEFORE`, `AFTER`, and `BETWEEN`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `LAST | NEXT | NOW | PREVIOUS | THIS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeGranularity`  <a name="cfn-quicksight-topic-topicrelativedatefilter-timegranularity"></a>
The level of time precision that is used to aggregate `DateTime` values\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DAY | HOUR | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)