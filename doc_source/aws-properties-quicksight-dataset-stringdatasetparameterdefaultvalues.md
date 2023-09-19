# AWS::QuickSight::DataSet StringDatasetParameterDefaultValues<a name="aws-properties-quicksight-dataset-stringdatasetparameterdefaultvalues"></a>

A list of default values for a given string dataset parameter type\. This structure only accepts static values\.

## Syntax<a name="aws-properties-quicksight-dataset-stringdatasetparameterdefaultvalues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-stringdatasetparameterdefaultvalues-syntax.json"></a>

```
{
  "[StaticValues](#cfn-quicksight-dataset-stringdatasetparameterdefaultvalues-staticvalues)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dataset-stringdatasetparameterdefaultvalues-syntax.yaml"></a>

```
  [StaticValues](#cfn-quicksight-dataset-stringdatasetparameterdefaultvalues-staticvalues): 
    - String
```

## Properties<a name="aws-properties-quicksight-dataset-stringdatasetparameterdefaultvalues-properties"></a>

`StaticValues`  <a name="cfn-quicksight-dataset-stringdatasetparameterdefaultvalues-staticvalues"></a>
A list of static default values for a given string parameter\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)