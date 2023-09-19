# AWS::QuickSight::DataSet DecimalDatasetParameterDefaultValues<a name="aws-properties-quicksight-dataset-decimaldatasetparameterdefaultvalues"></a>

A list of default values for a given decimal parameter\. This structure only accepts static values\.

## Syntax<a name="aws-properties-quicksight-dataset-decimaldatasetparameterdefaultvalues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-decimaldatasetparameterdefaultvalues-syntax.json"></a>

```
{
  "[StaticValues](#cfn-quicksight-dataset-decimaldatasetparameterdefaultvalues-staticvalues)" : [ Double, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dataset-decimaldatasetparameterdefaultvalues-syntax.yaml"></a>

```
  [StaticValues](#cfn-quicksight-dataset-decimaldatasetparameterdefaultvalues-staticvalues): 
    - Double
```

## Properties<a name="aws-properties-quicksight-dataset-decimaldatasetparameterdefaultvalues-properties"></a>

`StaticValues`  <a name="cfn-quicksight-dataset-decimaldatasetparameterdefaultvalues-staticvalues"></a>
A list of static default values for a given decimal parameter\.  
*Required*: No  
*Type*: List of Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)