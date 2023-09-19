# AWS::QuickSight::DataSet DecimalDatasetParameter<a name="aws-properties-quicksight-dataset-decimaldatasetparameter"></a>

A decimal parameter that is created in the dataset\.

## Syntax<a name="aws-properties-quicksight-dataset-decimaldatasetparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-decimaldatasetparameter-syntax.json"></a>

```
{
  "[DefaultValues](#cfn-quicksight-dataset-decimaldatasetparameter-defaultvalues)" : DecimalDatasetParameterDefaultValues,
  "[Id](#cfn-quicksight-dataset-decimaldatasetparameter-id)" : String,
  "[Name](#cfn-quicksight-dataset-decimaldatasetparameter-name)" : String,
  "[ValueType](#cfn-quicksight-dataset-decimaldatasetparameter-valuetype)" : String
}
```

### YAML<a name="aws-properties-quicksight-dataset-decimaldatasetparameter-syntax.yaml"></a>

```
  [DefaultValues](#cfn-quicksight-dataset-decimaldatasetparameter-defaultvalues): 
    DecimalDatasetParameterDefaultValues
  [Id](#cfn-quicksight-dataset-decimaldatasetparameter-id): String
  [Name](#cfn-quicksight-dataset-decimaldatasetparameter-name): String
  [ValueType](#cfn-quicksight-dataset-decimaldatasetparameter-valuetype): String
```

## Properties<a name="aws-properties-quicksight-dataset-decimaldatasetparameter-properties"></a>

`DefaultValues`  <a name="cfn-quicksight-dataset-decimaldatasetparameter-defaultvalues"></a>
A list of default values for a given decimal parameter\. This structure only accepts static values\.  
*Required*: No  
*Type*: [DecimalDatasetParameterDefaultValues](aws-properties-quicksight-dataset-decimaldatasetparameterdefaultvalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-quicksight-dataset-decimaldatasetparameter-id"></a>
An identifier for the decimal parameter created in the dataset\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-dataset-decimaldatasetparameter-name"></a>
The name of the decimal parameter that is created in the dataset\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueType`  <a name="cfn-quicksight-dataset-decimaldatasetparameter-valuetype"></a>
The value type of the dataset parameter\. Valid values are `single value` or `multi value`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)