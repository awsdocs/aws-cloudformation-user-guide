# AWS::QuickSight::DataSet DatasetParameter<a name="aws-properties-quicksight-dataset-datasetparameter"></a>

The parameter declarations of the dataset\.

## Syntax<a name="aws-properties-quicksight-dataset-datasetparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-datasetparameter-syntax.json"></a>

```
{
  "[DateTimeDatasetParameter](#cfn-quicksight-dataset-datasetparameter-datetimedatasetparameter)" : DateTimeDatasetParameter,
  "[DecimalDatasetParameter](#cfn-quicksight-dataset-datasetparameter-decimaldatasetparameter)" : DecimalDatasetParameter,
  "[IntegerDatasetParameter](#cfn-quicksight-dataset-datasetparameter-integerdatasetparameter)" : IntegerDatasetParameter,
  "[StringDatasetParameter](#cfn-quicksight-dataset-datasetparameter-stringdatasetparameter)" : StringDatasetParameter
}
```

### YAML<a name="aws-properties-quicksight-dataset-datasetparameter-syntax.yaml"></a>

```
  [DateTimeDatasetParameter](#cfn-quicksight-dataset-datasetparameter-datetimedatasetparameter): 
    DateTimeDatasetParameter
  [DecimalDatasetParameter](#cfn-quicksight-dataset-datasetparameter-decimaldatasetparameter): 
    DecimalDatasetParameter
  [IntegerDatasetParameter](#cfn-quicksight-dataset-datasetparameter-integerdatasetparameter): 
    IntegerDatasetParameter
  [StringDatasetParameter](#cfn-quicksight-dataset-datasetparameter-stringdatasetparameter): 
    StringDatasetParameter
```

## Properties<a name="aws-properties-quicksight-dataset-datasetparameter-properties"></a>

`DateTimeDatasetParameter`  <a name="cfn-quicksight-dataset-datasetparameter-datetimedatasetparameter"></a>
A date time parameter that is created in the dataset\.  
*Required*: No  
*Type*: [DateTimeDatasetParameter](aws-properties-quicksight-dataset-datetimedatasetparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DecimalDatasetParameter`  <a name="cfn-quicksight-dataset-datasetparameter-decimaldatasetparameter"></a>
A decimal parameter that is created in the dataset\.  
*Required*: No  
*Type*: [DecimalDatasetParameter](aws-properties-quicksight-dataset-decimaldatasetparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegerDatasetParameter`  <a name="cfn-quicksight-dataset-datasetparameter-integerdatasetparameter"></a>
An integer parameter that is created in the dataset\.  
*Required*: No  
*Type*: [IntegerDatasetParameter](aws-properties-quicksight-dataset-integerdatasetparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringDatasetParameter`  <a name="cfn-quicksight-dataset-datasetparameter-stringdatasetparameter"></a>
A string parameter that is created in the dataset\.  
*Required*: No  
*Type*: [StringDatasetParameter](aws-properties-quicksight-dataset-stringdatasetparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)