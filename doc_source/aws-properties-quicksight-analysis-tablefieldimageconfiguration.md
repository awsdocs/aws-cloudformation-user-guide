# AWS::QuickSight::Analysis TableFieldImageConfiguration<a name="aws-properties-quicksight-analysis-tablefieldimageconfiguration"></a>

The image configuration of a table field URL\.

## Syntax<a name="aws-properties-quicksight-analysis-tablefieldimageconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-tablefieldimageconfiguration-syntax.json"></a>

```
{
  "[SizingOptions](#cfn-quicksight-analysis-tablefieldimageconfiguration-sizingoptions)" : TableCellImageSizingConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-tablefieldimageconfiguration-syntax.yaml"></a>

```
  [SizingOptions](#cfn-quicksight-analysis-tablefieldimageconfiguration-sizingoptions): 
    TableCellImageSizingConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-tablefieldimageconfiguration-properties"></a>

`SizingOptions`  <a name="cfn-quicksight-analysis-tablefieldimageconfiguration-sizingoptions"></a>
The sizing options for the table image configuration\.  
*Required*: No  
*Type*: [TableCellImageSizingConfiguration](aws-properties-quicksight-analysis-tablecellimagesizingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)