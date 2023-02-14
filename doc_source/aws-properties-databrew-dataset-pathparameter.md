# AWS::DataBrew::Dataset PathParameter<a name="aws-properties-databrew-dataset-pathparameter"></a>

Represents a single entry in the path parameters of a dataset\. Each `PathParameter` consists of a name and a parameter definition\.

## Syntax<a name="aws-properties-databrew-dataset-pathparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-dataset-pathparameter-syntax.json"></a>

```
{
  "[DatasetParameter](#cfn-databrew-dataset-pathparameter-datasetparameter)" : DatasetParameter,
  "[PathParameterName](#cfn-databrew-dataset-pathparameter-pathparametername)" : String
}
```

### YAML<a name="aws-properties-databrew-dataset-pathparameter-syntax.yaml"></a>

```
  [DatasetParameter](#cfn-databrew-dataset-pathparameter-datasetparameter): 
    DatasetParameter
  [PathParameterName](#cfn-databrew-dataset-pathparameter-pathparametername): String
```

## Properties<a name="aws-properties-databrew-dataset-pathparameter-properties"></a>

`DatasetParameter`  <a name="cfn-databrew-dataset-pathparameter-datasetparameter"></a>
The path parameter definition\.  
*Required*: Yes  
*Type*: [DatasetParameter](aws-properties-databrew-dataset-datasetparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PathParameterName`  <a name="cfn-databrew-dataset-pathparameter-pathparametername"></a>
The name of the path parameter\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)