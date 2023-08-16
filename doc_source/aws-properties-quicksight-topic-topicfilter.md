# AWS::QuickSight::Topic TopicFilter<a name="aws-properties-quicksight-topic-topicfilter"></a>

A structure that represents a filter used to select items for a topic\.

## Syntax<a name="aws-properties-quicksight-topic-topicfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-topicfilter-syntax.json"></a>

```
{
  "[CategoryFilter](#cfn-quicksight-topic-topicfilter-categoryfilter)" : TopicCategoryFilter,
  "[DateRangeFilter](#cfn-quicksight-topic-topicfilter-daterangefilter)" : TopicDateRangeFilter,
  "[FilterClass](#cfn-quicksight-topic-topicfilter-filterclass)" : String,
  "[FilterDescription](#cfn-quicksight-topic-topicfilter-filterdescription)" : String,
  "[FilterName](#cfn-quicksight-topic-topicfilter-filtername)" : String,
  "[FilterSynonyms](#cfn-quicksight-topic-topicfilter-filtersynonyms)" : [ String, ... ],
  "[FilterType](#cfn-quicksight-topic-topicfilter-filtertype)" : String,
  "[NumericEqualityFilter](#cfn-quicksight-topic-topicfilter-numericequalityfilter)" : TopicNumericEqualityFilter,
  "[NumericRangeFilter](#cfn-quicksight-topic-topicfilter-numericrangefilter)" : TopicNumericRangeFilter,
  "[OperandFieldName](#cfn-quicksight-topic-topicfilter-operandfieldname)" : String,
  "[RelativeDateFilter](#cfn-quicksight-topic-topicfilter-relativedatefilter)" : TopicRelativeDateFilter
}
```

### YAML<a name="aws-properties-quicksight-topic-topicfilter-syntax.yaml"></a>

```
  [CategoryFilter](#cfn-quicksight-topic-topicfilter-categoryfilter): 
    TopicCategoryFilter
  [DateRangeFilter](#cfn-quicksight-topic-topicfilter-daterangefilter): 
    TopicDateRangeFilter
  [FilterClass](#cfn-quicksight-topic-topicfilter-filterclass): String
  [FilterDescription](#cfn-quicksight-topic-topicfilter-filterdescription): String
  [FilterName](#cfn-quicksight-topic-topicfilter-filtername): String
  [FilterSynonyms](#cfn-quicksight-topic-topicfilter-filtersynonyms): 
    - String
  [FilterType](#cfn-quicksight-topic-topicfilter-filtertype): String
  [NumericEqualityFilter](#cfn-quicksight-topic-topicfilter-numericequalityfilter): 
    TopicNumericEqualityFilter
  [NumericRangeFilter](#cfn-quicksight-topic-topicfilter-numericrangefilter): 
    TopicNumericRangeFilter
  [OperandFieldName](#cfn-quicksight-topic-topicfilter-operandfieldname): String
  [RelativeDateFilter](#cfn-quicksight-topic-topicfilter-relativedatefilter): 
    TopicRelativeDateFilter
```

## Properties<a name="aws-properties-quicksight-topic-topicfilter-properties"></a>

`CategoryFilter`  <a name="cfn-quicksight-topic-topicfilter-categoryfilter"></a>
The category filter that is associated with this filter\.  
*Required*: No  
*Type*: [TopicCategoryFilter](aws-properties-quicksight-topic-topiccategoryfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DateRangeFilter`  <a name="cfn-quicksight-topic-topicfilter-daterangefilter"></a>
The date range filter\.  
*Required*: No  
*Type*: [TopicDateRangeFilter](aws-properties-quicksight-topic-topicdaterangefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterClass`  <a name="cfn-quicksight-topic-topicfilter-filterclass"></a>
The class of the filter\. Valid values for this structure are `ENFORCED_VALUE_FILTER`, `CONDITIONAL_VALUE_FILTER`, and `NAMED_VALUE_FILTER`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CONDITIONAL_VALUE_FILTER | ENFORCED_VALUE_FILTER | NAMED_VALUE_FILTER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterDescription`  <a name="cfn-quicksight-topic-topicfilter-filterdescription"></a>
A description of the filter used to select items for a topic\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterName`  <a name="cfn-quicksight-topic-topicfilter-filtername"></a>
The name of the filter\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterSynonyms`  <a name="cfn-quicksight-topic-topicfilter-filtersynonyms"></a>
The other names or aliases for the filter\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterType`  <a name="cfn-quicksight-topic-topicfilter-filtertype"></a>
The type of the filter\. Valid values for this structure are `CATEGORY_FILTER`, `NUMERIC_EQUALITY_FILTER`, `NUMERIC_RANGE_FILTER`, `DATE_RANGE_FILTER`, and `RELATIVE_DATE_FILTER`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CATEGORY_FILTER | DATE_RANGE_FILTER | NUMERIC_EQUALITY_FILTER | NUMERIC_RANGE_FILTER | RELATIVE_DATE_FILTER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumericEqualityFilter`  <a name="cfn-quicksight-topic-topicfilter-numericequalityfilter"></a>
The numeric equality filter\.  
*Required*: No  
*Type*: [TopicNumericEqualityFilter](aws-properties-quicksight-topic-topicnumericequalityfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumericRangeFilter`  <a name="cfn-quicksight-topic-topicfilter-numericrangefilter"></a>
The numeric range filter\.  
*Required*: No  
*Type*: [TopicNumericRangeFilter](aws-properties-quicksight-topic-topicnumericrangefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OperandFieldName`  <a name="cfn-quicksight-topic-topicfilter-operandfieldname"></a>
The name of the field that the filter operates on\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelativeDateFilter`  <a name="cfn-quicksight-topic-topicfilter-relativedatefilter"></a>
The relative date filter\.  
*Required*: No  
*Type*: [TopicRelativeDateFilter](aws-properties-quicksight-topic-topicrelativedatefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)