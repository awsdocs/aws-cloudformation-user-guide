# AWS::QuickSight::DataSet IntegerDatasetParameterDefaultValues<a name="aws-properties-quicksight-dataset-integerdatasetparameterdefaultvalues"></a>

A list of default values for a given integer parameter\. This structure only accepts static values\.

## Syntax<a name="aws-properties-quicksight-dataset-integerdatasetparameterdefaultvalues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-integerdatasetparameterdefaultvalues-syntax.json"></a>

```
{
  "[StaticValues](#cfn-quicksight-dataset-integerdatasetparameterdefaultvalues-staticvalues)" : [ Double, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dataset-integerdatasetparameterdefaultvalues-syntax.yaml"></a>

```
  [StaticValues](#cfn-quicksight-dataset-integerdatasetparameterdefaultvalues-staticvalues): 
    - Double
```

## Properties<a name="aws-properties-quicksight-dataset-integerdatasetparameterdefaultvalues-properties"></a>

`StaticValues`  <a name="cfn-quicksight-dataset-integerdatasetparameterdefaultvalues-staticvalues"></a>
A list of static default values for a given integer parameter\.  
*Required*: No  
*Type*: List of Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)