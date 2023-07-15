# AWS::QuickSight::DataSet OverrideDatasetParameterOperation<a name="aws-properties-quicksight-dataset-overridedatasetparameteroperation"></a>

A transform operation that overrides the dataset parameter values that are defined in another dataset\.

## Syntax<a name="aws-properties-quicksight-dataset-overridedatasetparameteroperation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-overridedatasetparameteroperation-syntax.json"></a>

```
{
  "[NewDefaultValues](#cfn-quicksight-dataset-overridedatasetparameteroperation-newdefaultvalues)" : NewDefaultValues,
  "[NewParameterName](#cfn-quicksight-dataset-overridedatasetparameteroperation-newparametername)" : String,
  "[ParameterName](#cfn-quicksight-dataset-overridedatasetparameteroperation-parametername)" : String
}
```

### YAML<a name="aws-properties-quicksight-dataset-overridedatasetparameteroperation-syntax.yaml"></a>

```
  [NewDefaultValues](#cfn-quicksight-dataset-overridedatasetparameteroperation-newdefaultvalues): 
    NewDefaultValues
  [NewParameterName](#cfn-quicksight-dataset-overridedatasetparameteroperation-newparametername): String
  [ParameterName](#cfn-quicksight-dataset-overridedatasetparameteroperation-parametername): String
```

## Properties<a name="aws-properties-quicksight-dataset-overridedatasetparameteroperation-properties"></a>

`NewDefaultValues`  <a name="cfn-quicksight-dataset-overridedatasetparameteroperation-newdefaultvalues"></a>
The new default values for the parameter\.  
*Required*: No  
*Type*: [NewDefaultValues](aws-properties-quicksight-dataset-newdefaultvalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NewParameterName`  <a name="cfn-quicksight-dataset-overridedatasetparameteroperation-newparametername"></a>
The new name for the parameter\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterName`  <a name="cfn-quicksight-dataset-overridedatasetparameteroperation-parametername"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)