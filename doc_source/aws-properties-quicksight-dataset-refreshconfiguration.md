# AWS::QuickSight::DataSet RefreshConfiguration<a name="aws-properties-quicksight-dataset-refreshconfiguration"></a>

The refresh configuration of a dataset\.

## Syntax<a name="aws-properties-quicksight-dataset-refreshconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-refreshconfiguration-syntax.json"></a>

```
{
  "[IncrementalRefresh](#cfn-quicksight-dataset-refreshconfiguration-incrementalrefresh)" : IncrementalRefresh
}
```

### YAML<a name="aws-properties-quicksight-dataset-refreshconfiguration-syntax.yaml"></a>

```
  [IncrementalRefresh](#cfn-quicksight-dataset-refreshconfiguration-incrementalrefresh): 
    IncrementalRefresh
```

## Properties<a name="aws-properties-quicksight-dataset-refreshconfiguration-properties"></a>

`IncrementalRefresh`  <a name="cfn-quicksight-dataset-refreshconfiguration-incrementalrefresh"></a>
The incremental refresh for the dataset\.  
*Required*: No  
*Type*: [IncrementalRefresh](aws-properties-quicksight-dataset-incrementalrefresh.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)