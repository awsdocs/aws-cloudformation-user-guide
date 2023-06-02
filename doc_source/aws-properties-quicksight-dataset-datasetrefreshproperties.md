# AWS::QuickSight::DataSet DataSetRefreshProperties<a name="aws-properties-quicksight-dataset-datasetrefreshproperties"></a>

The refresh properties of a dataset\.

## Syntax<a name="aws-properties-quicksight-dataset-datasetrefreshproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-datasetrefreshproperties-syntax.json"></a>

```
{
  "[RefreshConfiguration](#cfn-quicksight-dataset-datasetrefreshproperties-refreshconfiguration)" : RefreshConfiguration
}
```

### YAML<a name="aws-properties-quicksight-dataset-datasetrefreshproperties-syntax.yaml"></a>

```
  [RefreshConfiguration](#cfn-quicksight-dataset-datasetrefreshproperties-refreshconfiguration): 
    RefreshConfiguration
```

## Properties<a name="aws-properties-quicksight-dataset-datasetrefreshproperties-properties"></a>

`RefreshConfiguration`  <a name="cfn-quicksight-dataset-datasetrefreshproperties-refreshconfiguration"></a>
The refresh configuration for a dataset\.  
*Required*: No  
*Type*: [RefreshConfiguration](aws-properties-quicksight-dataset-refreshconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)