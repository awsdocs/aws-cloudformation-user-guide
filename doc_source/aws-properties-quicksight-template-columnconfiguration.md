# AWS::QuickSight::Template ColumnConfiguration<a name="aws-properties-quicksight-template-columnconfiguration"></a>

The general configuration of a column\.

## Syntax<a name="aws-properties-quicksight-template-columnconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-columnconfiguration-syntax.json"></a>

```
{
  "[ColorsConfiguration](#cfn-quicksight-template-columnconfiguration-colorsconfiguration)" : ColorsConfiguration,
  "[Column](#cfn-quicksight-template-columnconfiguration-column)" : ColumnIdentifier,
  "[FormatConfiguration](#cfn-quicksight-template-columnconfiguration-formatconfiguration)" : FormatConfiguration,
  "[Role](#cfn-quicksight-template-columnconfiguration-role)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-columnconfiguration-syntax.yaml"></a>

```
  [ColorsConfiguration](#cfn-quicksight-template-columnconfiguration-colorsconfiguration): 
    ColorsConfiguration
  [Column](#cfn-quicksight-template-columnconfiguration-column): 
    ColumnIdentifier
  [FormatConfiguration](#cfn-quicksight-template-columnconfiguration-formatconfiguration): 
    FormatConfiguration
  [Role](#cfn-quicksight-template-columnconfiguration-role): String
```

## Properties<a name="aws-properties-quicksight-template-columnconfiguration-properties"></a>

`ColorsConfiguration`  <a name="cfn-quicksight-template-columnconfiguration-colorsconfiguration"></a>
The color configurations of the column\.  
*Required*: No  
*Type*: [ColorsConfiguration](aws-properties-quicksight-template-colorsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Column`  <a name="cfn-quicksight-template-columnconfiguration-column"></a>
The column\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FormatConfiguration`  <a name="cfn-quicksight-template-columnconfiguration-formatconfiguration"></a>
The format configuration of a column\.  
*Required*: No  
*Type*: [FormatConfiguration](aws-properties-quicksight-template-formatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Role`  <a name="cfn-quicksight-template-columnconfiguration-role"></a>
The role of the column\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DIMENSION | MEASURE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)