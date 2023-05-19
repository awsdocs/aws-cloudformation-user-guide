# AWS::QuickSight::Topic TopicCalculatedField<a name="aws-properties-quicksight-topic-topiccalculatedfield"></a>

A structure that represents a calculated field\.

## Syntax<a name="aws-properties-quicksight-topic-topiccalculatedfield-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-topiccalculatedfield-syntax.json"></a>

```
{
  "[Aggregation](#cfn-quicksight-topic-topiccalculatedfield-aggregation)" : String,
  "[AllowedAggregations](#cfn-quicksight-topic-topiccalculatedfield-allowedaggregations)" : [ String, ... ],
  "[CalculatedFieldDescription](#cfn-quicksight-topic-topiccalculatedfield-calculatedfielddescription)" : String,
  "[CalculatedFieldName](#cfn-quicksight-topic-topiccalculatedfield-calculatedfieldname)" : String,
  "[CalculatedFieldSynonyms](#cfn-quicksight-topic-topiccalculatedfield-calculatedfieldsynonyms)" : [ String, ... ],
  "[CellValueSynonyms](#cfn-quicksight-topic-topiccalculatedfield-cellvaluesynonyms)" : [ CellValueSynonym, ... ],
  "[ColumnDataRole](#cfn-quicksight-topic-topiccalculatedfield-columndatarole)" : String,
  "[ComparativeOrder](#cfn-quicksight-topic-topiccalculatedfield-comparativeorder)" : ComparativeOrder,
  "[DefaultFormatting](#cfn-quicksight-topic-topiccalculatedfield-defaultformatting)" : DefaultFormatting,
  "[Expression](#cfn-quicksight-topic-topiccalculatedfield-expression)" : String,
  "[IsIncludedInTopic](#cfn-quicksight-topic-topiccalculatedfield-isincludedintopic)" : Boolean,
  "[NeverAggregateInFilter](#cfn-quicksight-topic-topiccalculatedfield-neveraggregateinfilter)" : Boolean,
  "[NotAllowedAggregations](#cfn-quicksight-topic-topiccalculatedfield-notallowedaggregations)" : [ String, ... ],
  "[SemanticType](#cfn-quicksight-topic-topiccalculatedfield-semantictype)" : SemanticType,
  "[TimeGranularity](#cfn-quicksight-topic-topiccalculatedfield-timegranularity)" : String
}
```

### YAML<a name="aws-properties-quicksight-topic-topiccalculatedfield-syntax.yaml"></a>

```
  [Aggregation](#cfn-quicksight-topic-topiccalculatedfield-aggregation): String
  [AllowedAggregations](#cfn-quicksight-topic-topiccalculatedfield-allowedaggregations): 
    - String
  [CalculatedFieldDescription](#cfn-quicksight-topic-topiccalculatedfield-calculatedfielddescription): String
  [CalculatedFieldName](#cfn-quicksight-topic-topiccalculatedfield-calculatedfieldname): String
  [CalculatedFieldSynonyms](#cfn-quicksight-topic-topiccalculatedfield-calculatedfieldsynonyms): 
    - String
  [CellValueSynonyms](#cfn-quicksight-topic-topiccalculatedfield-cellvaluesynonyms): 
    - CellValueSynonym
  [ColumnDataRole](#cfn-quicksight-topic-topiccalculatedfield-columndatarole): String
  [ComparativeOrder](#cfn-quicksight-topic-topiccalculatedfield-comparativeorder): 
    ComparativeOrder
  [DefaultFormatting](#cfn-quicksight-topic-topiccalculatedfield-defaultformatting): 
    DefaultFormatting
  [Expression](#cfn-quicksight-topic-topiccalculatedfield-expression): String
  [IsIncludedInTopic](#cfn-quicksight-topic-topiccalculatedfield-isincludedintopic): Boolean
  [NeverAggregateInFilter](#cfn-quicksight-topic-topiccalculatedfield-neveraggregateinfilter): Boolean
  [NotAllowedAggregations](#cfn-quicksight-topic-topiccalculatedfield-notallowedaggregations): 
    - String
  [SemanticType](#cfn-quicksight-topic-topiccalculatedfield-semantictype): 
    SemanticType
  [TimeGranularity](#cfn-quicksight-topic-topiccalculatedfield-timegranularity): String
```

## Properties<a name="aws-properties-quicksight-topic-topiccalculatedfield-properties"></a>

`Aggregation`  <a name="cfn-quicksight-topic-topiccalculatedfield-aggregation"></a>
The default aggregation\. Valid values for this structure are `SUM`, `MAX`, `MIN`, `COUNT`, `DISTINCT_COUNT`, and `AVERAGE`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AVERAGE | COUNT | DISTINCT_COUNT | MAX | MIN | SUM`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowedAggregations`  <a name="cfn-quicksight-topic-topiccalculatedfield-allowedaggregations"></a>
The list of aggregation types that are allowed for the calculated field\. Valid values for this structure are `COUNT`, `DISTINCT_COUNT`, `MIN`, `MAX`, `MEDIAN`, `SUM`, `AVERAGE`, `STDEV`, `STDEVP`, `VAR`, `VARP`, and `PERCENTILE`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CalculatedFieldDescription`  <a name="cfn-quicksight-topic-topiccalculatedfield-calculatedfielddescription"></a>
The calculated field description\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CalculatedFieldName`  <a name="cfn-quicksight-topic-topiccalculatedfield-calculatedfieldname"></a>
The calculated field name\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CalculatedFieldSynonyms`  <a name="cfn-quicksight-topic-topiccalculatedfield-calculatedfieldsynonyms"></a>
The other names or aliases for the calculated field\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CellValueSynonyms`  <a name="cfn-quicksight-topic-topiccalculatedfield-cellvaluesynonyms"></a>
The other names or aliases for the calculated field cell value\.  
*Required*: No  
*Type*: List of [CellValueSynonym](aws-properties-quicksight-topic-cellvaluesynonym.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnDataRole`  <a name="cfn-quicksight-topic-topiccalculatedfield-columndatarole"></a>
The column data role for a calculated field\. Valid values for this structure are `DIMENSION` and `MEASURE`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DIMENSION | MEASURE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComparativeOrder`  <a name="cfn-quicksight-topic-topiccalculatedfield-comparativeorder"></a>
The order in which data is displayed for the calculated field when it's used in a comparative context\.  
*Required*: No  
*Type*: [ComparativeOrder](aws-properties-quicksight-topic-comparativeorder.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultFormatting`  <a name="cfn-quicksight-topic-topiccalculatedfield-defaultformatting"></a>
The default formatting definition\.  
*Required*: No  
*Type*: [DefaultFormatting](aws-properties-quicksight-topic-defaultformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expression`  <a name="cfn-quicksight-topic-topiccalculatedfield-expression"></a>
The calculated field expression\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsIncludedInTopic`  <a name="cfn-quicksight-topic-topiccalculatedfield-isincludedintopic"></a>
A boolean value that indicates if a calculated field is included in the topic\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NeverAggregateInFilter`  <a name="cfn-quicksight-topic-topiccalculatedfield-neveraggregateinfilter"></a>
A Boolean value that indicates whether to never aggregate calculated field in filters\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotAllowedAggregations`  <a name="cfn-quicksight-topic-topiccalculatedfield-notallowedaggregations"></a>
The list of aggregation types that are not allowed for the calculated field\. Valid values for this structure are `COUNT`, `DISTINCT_COUNT`, `MIN`, `MAX`, `MEDIAN`, `SUM`, `AVERAGE`, `STDEV`, `STDEVP`, `VAR`, `VARP`, and `PERCENTILE`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SemanticType`  <a name="cfn-quicksight-topic-topiccalculatedfield-semantictype"></a>
The semantic type\.  
*Required*: No  
*Type*: [SemanticType](aws-properties-quicksight-topic-semantictype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeGranularity`  <a name="cfn-quicksight-topic-topiccalculatedfield-timegranularity"></a>
The level of time precision that is used to aggregate `DateTime` values\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DAY | HOUR | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)