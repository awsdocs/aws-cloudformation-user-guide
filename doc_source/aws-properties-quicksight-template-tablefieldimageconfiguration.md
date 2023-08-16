# AWS::QuickSight::Template TableFieldImageConfiguration<a name="aws-properties-quicksight-template-tablefieldimageconfiguration"></a>

The image configuration of a table field URL\.

## Syntax<a name="aws-properties-quicksight-template-tablefieldimageconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-tablefieldimageconfiguration-syntax.json"></a>

```
{
  "[SizingOptions](#cfn-quicksight-template-tablefieldimageconfiguration-sizingoptions)" : TableCellImageSizingConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-tablefieldimageconfiguration-syntax.yaml"></a>

```
  [SizingOptions](#cfn-quicksight-template-tablefieldimageconfiguration-sizingoptions): 
    TableCellImageSizingConfiguration
```

## Properties<a name="aws-properties-quicksight-template-tablefieldimageconfiguration-properties"></a>

`SizingOptions`  <a name="cfn-quicksight-template-tablefieldimageconfiguration-sizingoptions"></a>
The sizing options for the table image configuration\.  
*Required*: No  
*Type*: [TableCellImageSizingConfiguration](aws-properties-quicksight-template-tablecellimagesizingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)