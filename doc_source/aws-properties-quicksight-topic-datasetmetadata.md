# AWS::QuickSight::Topic DatasetMetadata<a name="aws-properties-quicksight-topic-datasetmetadata"></a>

A structure that represents a dataset\.

## Syntax<a name="aws-properties-quicksight-topic-datasetmetadata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-datasetmetadata-syntax.json"></a>

```
{
  "[CalculatedFields](#cfn-quicksight-topic-datasetmetadata-calculatedfields)" : [ TopicCalculatedField, ... ],
  "[Columns](#cfn-quicksight-topic-datasetmetadata-columns)" : [ TopicColumn, ... ],
  "[DataAggregation](#cfn-quicksight-topic-datasetmetadata-dataaggregation)" : DataAggregation,
  "[DatasetArn](#cfn-quicksight-topic-datasetmetadata-datasetarn)" : String,
  "[DatasetDescription](#cfn-quicksight-topic-datasetmetadata-datasetdescription)" : String,
  "[DatasetName](#cfn-quicksight-topic-datasetmetadata-datasetname)" : String,
  "[Filters](#cfn-quicksight-topic-datasetmetadata-filters)" : [ TopicFilter, ... ],
  "[NamedEntities](#cfn-quicksight-topic-datasetmetadata-namedentities)" : [ TopicNamedEntity, ... ]
}
```

### YAML<a name="aws-properties-quicksight-topic-datasetmetadata-syntax.yaml"></a>

```
  [CalculatedFields](#cfn-quicksight-topic-datasetmetadata-calculatedfields): 
    - TopicCalculatedField
  [Columns](#cfn-quicksight-topic-datasetmetadata-columns): 
    - TopicColumn
  [DataAggregation](#cfn-quicksight-topic-datasetmetadata-dataaggregation): 
    DataAggregation
  [DatasetArn](#cfn-quicksight-topic-datasetmetadata-datasetarn): String
  [DatasetDescription](#cfn-quicksight-topic-datasetmetadata-datasetdescription): String
  [DatasetName](#cfn-quicksight-topic-datasetmetadata-datasetname): String
  [Filters](#cfn-quicksight-topic-datasetmetadata-filters): 
    - TopicFilter
  [NamedEntities](#cfn-quicksight-topic-datasetmetadata-namedentities): 
    - TopicNamedEntity
```

## Properties<a name="aws-properties-quicksight-topic-datasetmetadata-properties"></a>

`CalculatedFields`  <a name="cfn-quicksight-topic-datasetmetadata-calculatedfields"></a>
The list of calculated field definitions\.  
*Required*: No  
*Type*: List of [TopicCalculatedField](aws-properties-quicksight-topic-topiccalculatedfield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Columns`  <a name="cfn-quicksight-topic-datasetmetadata-columns"></a>
The list of column definitions\.  
*Required*: No  
*Type*: List of [TopicColumn](aws-properties-quicksight-topic-topiccolumn.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataAggregation`  <a name="cfn-quicksight-topic-datasetmetadata-dataaggregation"></a>
The definition of a data aggregation\.  
*Required*: No  
*Type*: [DataAggregation](aws-properties-quicksight-topic-dataaggregation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatasetArn`  <a name="cfn-quicksight-topic-datasetmetadata-datasetarn"></a>
The Amazon Resource Name \(ARN\) of the dataset\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatasetDescription`  <a name="cfn-quicksight-topic-datasetmetadata-datasetdescription"></a>
The description of the dataset\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatasetName`  <a name="cfn-quicksight-topic-datasetmetadata-datasetname"></a>
The name of the dataset\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Filters`  <a name="cfn-quicksight-topic-datasetmetadata-filters"></a>
The list of filter definitions\.  
*Required*: No  
*Type*: List of [TopicFilter](aws-properties-quicksight-topic-topicfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NamedEntities`  <a name="cfn-quicksight-topic-datasetmetadata-namedentities"></a>
The list of named entities definitions\.  
*Required*: No  
*Type*: List of [TopicNamedEntity](aws-properties-quicksight-topic-topicnamedentity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)