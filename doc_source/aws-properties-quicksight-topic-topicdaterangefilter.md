# AWS::QuickSight::Topic TopicDateRangeFilter<a name="aws-properties-quicksight-topic-topicdaterangefilter"></a>

A filter used to restrict data based on a range of dates or times\.

## Syntax<a name="aws-properties-quicksight-topic-topicdaterangefilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-topicdaterangefilter-syntax.json"></a>

```
{
  "[Constant](#cfn-quicksight-topic-topicdaterangefilter-constant)" : TopicRangeFilterConstant,
  "[Inclusive](#cfn-quicksight-topic-topicdaterangefilter-inclusive)" : Boolean
}
```

### YAML<a name="aws-properties-quicksight-topic-topicdaterangefilter-syntax.yaml"></a>

```
  [Constant](#cfn-quicksight-topic-topicdaterangefilter-constant): 
    TopicRangeFilterConstant
  [Inclusive](#cfn-quicksight-topic-topicdaterangefilter-inclusive): Boolean
```

## Properties<a name="aws-properties-quicksight-topic-topicdaterangefilter-properties"></a>

`Constant`  <a name="cfn-quicksight-topic-topicdaterangefilter-constant"></a>
The constant used in a date range filter\.  
*Required*: No  
*Type*: [TopicRangeFilterConstant](aws-properties-quicksight-topic-topicrangefilterconstant.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Inclusive`  <a name="cfn-quicksight-topic-topicdaterangefilter-inclusive"></a>
A Boolean value that indicates whether the date range filter should include the boundary values\. If set to true, the filter includes the start and end dates\. If set to false, the filter excludes them\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)