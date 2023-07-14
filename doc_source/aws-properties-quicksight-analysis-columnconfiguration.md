# AWS::QuickSight::Analysis ColumnConfiguration<a name="aws-properties-quicksight-analysis-columnconfiguration"></a>

The general configuration of a column\.

## Syntax<a name="aws-properties-quicksight-analysis-columnconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-columnconfiguration-syntax.json"></a>

```
{
  "[Column](#cfn-quicksight-analysis-columnconfiguration-column)" : ColumnIdentifier,
  "[FormatConfiguration](#cfn-quicksight-analysis-columnconfiguration-formatconfiguration)" : FormatConfiguration,
  "[Role](#cfn-quicksight-analysis-columnconfiguration-role)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-columnconfiguration-syntax.yaml"></a>

```
  [Column](#cfn-quicksight-analysis-columnconfiguration-column): 
    ColumnIdentifier
  [FormatConfiguration](#cfn-quicksight-analysis-columnconfiguration-formatconfiguration): 
    FormatConfiguration
  [Role](#cfn-quicksight-analysis-columnconfiguration-role): String
```

## Properties<a name="aws-properties-quicksight-analysis-columnconfiguration-properties"></a>

`Column`  <a name="cfn-quicksight-analysis-columnconfiguration-column"></a>
The column\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-analysis-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FormatConfiguration`  <a name="cfn-quicksight-analysis-columnconfiguration-formatconfiguration"></a>
The format configuration of a column\.  
*Required*: No  
*Type*: [FormatConfiguration](aws-properties-quicksight-analysis-formatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Role`  <a name="cfn-quicksight-analysis-columnconfiguration-role"></a>
The role of the column\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DIMENSION | MEASURE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)