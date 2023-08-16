# AWS::QuickSight::Template MappedDataSetParameter<a name="aws-properties-quicksight-template-mappeddatasetparameter"></a>

A dataset parameter that is mapped to an analysis parameter\.

## Syntax<a name="aws-properties-quicksight-template-mappeddatasetparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-mappeddatasetparameter-syntax.json"></a>

```
{
  "[DataSetIdentifier](#cfn-quicksight-template-mappeddatasetparameter-datasetidentifier)" : String,
  "[DataSetParameterName](#cfn-quicksight-template-mappeddatasetparameter-datasetparametername)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-mappeddatasetparameter-syntax.yaml"></a>

```
  [DataSetIdentifier](#cfn-quicksight-template-mappeddatasetparameter-datasetidentifier): String
  [DataSetParameterName](#cfn-quicksight-template-mappeddatasetparameter-datasetparametername): String
```

## Properties<a name="aws-properties-quicksight-template-mappeddatasetparameter-properties"></a>

`DataSetIdentifier`  <a name="cfn-quicksight-template-mappeddatasetparameter-datasetidentifier"></a>
A unique name that identifies a dataset within the analysis or dashboard\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSetParameterName`  <a name="cfn-quicksight-template-mappeddatasetparameter-datasetparametername"></a>
The name of the dataset parameter\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)