# AWS::QuickSight::DataSet DataSetUsageConfiguration<a name="aws-properties-quicksight-dataset-datasetusageconfiguration"></a>

The usage configuration to apply to child datasets that reference this dataset as a source\.

## Syntax<a name="aws-properties-quicksight-dataset-datasetusageconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-datasetusageconfiguration-syntax.json"></a>

```
{
  "[DisableUseAsDirectQuerySource](#cfn-quicksight-dataset-datasetusageconfiguration-disableuseasdirectquerysource)" : Boolean,
  "[DisableUseAsImportedSource](#cfn-quicksight-dataset-datasetusageconfiguration-disableuseasimportedsource)" : Boolean
}
```

### YAML<a name="aws-properties-quicksight-dataset-datasetusageconfiguration-syntax.yaml"></a>

```
  [DisableUseAsDirectQuerySource](#cfn-quicksight-dataset-datasetusageconfiguration-disableuseasdirectquerysource): Boolean
  [DisableUseAsImportedSource](#cfn-quicksight-dataset-datasetusageconfiguration-disableuseasimportedsource): Boolean
```

## Properties<a name="aws-properties-quicksight-dataset-datasetusageconfiguration-properties"></a>

`DisableUseAsDirectQuerySource`  <a name="cfn-quicksight-dataset-datasetusageconfiguration-disableuseasdirectquerysource"></a>
An option that controls whether a child dataset of a direct query can use this dataset as a source\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableUseAsImportedSource`  <a name="cfn-quicksight-dataset-datasetusageconfiguration-disableuseasimportedsource"></a>
An option that controls whether a child dataset that's stored in QuickSight can use this dataset as a source\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)