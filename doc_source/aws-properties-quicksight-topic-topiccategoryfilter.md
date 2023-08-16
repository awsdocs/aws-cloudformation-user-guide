# AWS::QuickSight::Topic TopicCategoryFilter<a name="aws-properties-quicksight-topic-topiccategoryfilter"></a>

A structure that represents a category filter\.

## Syntax<a name="aws-properties-quicksight-topic-topiccategoryfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-topiccategoryfilter-syntax.json"></a>

```
{
  "[CategoryFilterFunction](#cfn-quicksight-topic-topiccategoryfilter-categoryfilterfunction)" : String,
  "[CategoryFilterType](#cfn-quicksight-topic-topiccategoryfilter-categoryfiltertype)" : String,
  "[Constant](#cfn-quicksight-topic-topiccategoryfilter-constant)" : TopicCategoryFilterConstant,
  "[Inverse](#cfn-quicksight-topic-topiccategoryfilter-inverse)" : Boolean
}
```

### YAML<a name="aws-properties-quicksight-topic-topiccategoryfilter-syntax.yaml"></a>

```
  [CategoryFilterFunction](#cfn-quicksight-topic-topiccategoryfilter-categoryfilterfunction): String
  [CategoryFilterType](#cfn-quicksight-topic-topiccategoryfilter-categoryfiltertype): String
  [Constant](#cfn-quicksight-topic-topiccategoryfilter-constant): 
    TopicCategoryFilterConstant
  [Inverse](#cfn-quicksight-topic-topiccategoryfilter-inverse): Boolean
```

## Properties<a name="aws-properties-quicksight-topic-topiccategoryfilter-properties"></a>

`CategoryFilterFunction`  <a name="cfn-quicksight-topic-topiccategoryfilter-categoryfilterfunction"></a>
The category filter function\. Valid values for this structure are `EXACT` and `CONTAINS`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CONTAINS | EXACT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryFilterType`  <a name="cfn-quicksight-topic-topiccategoryfilter-categoryfiltertype"></a>
The category filter type\. This element is used to specify whether a filter is a simple category filter or an inverse category filter\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CUSTOM_FILTER | CUSTOM_FILTER_LIST | FILTER_LIST`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Constant`  <a name="cfn-quicksight-topic-topiccategoryfilter-constant"></a>
The constant used in a category filter\.  
*Required*: No  
*Type*: [TopicCategoryFilterConstant](aws-properties-quicksight-topic-topiccategoryfilterconstant.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Inverse`  <a name="cfn-quicksight-topic-topiccategoryfilter-inverse"></a>
A Boolean value that indicates if the filter is inverse\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)