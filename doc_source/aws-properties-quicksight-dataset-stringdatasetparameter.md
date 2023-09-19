# AWS::QuickSight::DataSet StringDatasetParameter<a name="aws-properties-quicksight-dataset-stringdatasetparameter"></a>

A string parameter that is created in the dataset\.

## Syntax<a name="aws-properties-quicksight-dataset-stringdatasetparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-stringdatasetparameter-syntax.json"></a>

```
{
  "[DefaultValues](#cfn-quicksight-dataset-stringdatasetparameter-defaultvalues)" : StringDatasetParameterDefaultValues,
  "[Id](#cfn-quicksight-dataset-stringdatasetparameter-id)" : String,
  "[Name](#cfn-quicksight-dataset-stringdatasetparameter-name)" : String,
  "[ValueType](#cfn-quicksight-dataset-stringdatasetparameter-valuetype)" : String
}
```

### YAML<a name="aws-properties-quicksight-dataset-stringdatasetparameter-syntax.yaml"></a>

```
  [DefaultValues](#cfn-quicksight-dataset-stringdatasetparameter-defaultvalues): 
    StringDatasetParameterDefaultValues
  [Id](#cfn-quicksight-dataset-stringdatasetparameter-id): String
  [Name](#cfn-quicksight-dataset-stringdatasetparameter-name): String
  [ValueType](#cfn-quicksight-dataset-stringdatasetparameter-valuetype): String
```

## Properties<a name="aws-properties-quicksight-dataset-stringdatasetparameter-properties"></a>

`DefaultValues`  <a name="cfn-quicksight-dataset-stringdatasetparameter-defaultvalues"></a>
A list of default values for a given string dataset parameter type\. This structure only accepts static values\.  
*Required*: No  
*Type*: [StringDatasetParameterDefaultValues](aws-properties-quicksight-dataset-stringdatasetparameterdefaultvalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-quicksight-dataset-stringdatasetparameter-id"></a>
An identifier for the string parameter that is created in the dataset\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-dataset-stringdatasetparameter-name"></a>
The name of the string parameter that is created in the dataset\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueType`  <a name="cfn-quicksight-dataset-stringdatasetparameter-valuetype"></a>
The value type of the dataset parameter\. Valid values are `single value` or `multi value`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)