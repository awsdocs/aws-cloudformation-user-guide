# AWS::QuickSight::Dashboard ColumnConfiguration<a name="aws-properties-quicksight-dashboard-columnconfiguration"></a>

The general configuration of a column\.

## Syntax<a name="aws-properties-quicksight-dashboard-columnconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-columnconfiguration-syntax.json"></a>

```
{
  "[ColorsConfiguration](#cfn-quicksight-dashboard-columnconfiguration-colorsconfiguration)" : ColorsConfiguration,
  "[Column](#cfn-quicksight-dashboard-columnconfiguration-column)" : ColumnIdentifier,
  "[FormatConfiguration](#cfn-quicksight-dashboard-columnconfiguration-formatconfiguration)" : FormatConfiguration,
  "[Role](#cfn-quicksight-dashboard-columnconfiguration-role)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-columnconfiguration-syntax.yaml"></a>

```
  [ColorsConfiguration](#cfn-quicksight-dashboard-columnconfiguration-colorsconfiguration): 
    ColorsConfiguration
  [Column](#cfn-quicksight-dashboard-columnconfiguration-column): 
    ColumnIdentifier
  [FormatConfiguration](#cfn-quicksight-dashboard-columnconfiguration-formatconfiguration): 
    FormatConfiguration
  [Role](#cfn-quicksight-dashboard-columnconfiguration-role): String
```

## Properties<a name="aws-properties-quicksight-dashboard-columnconfiguration-properties"></a>

`ColorsConfiguration`  <a name="cfn-quicksight-dashboard-columnconfiguration-colorsconfiguration"></a>
The color configurations of the column\.  
*Required*: No  
*Type*: [ColorsConfiguration](aws-properties-quicksight-dashboard-colorsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Column`  <a name="cfn-quicksight-dashboard-columnconfiguration-column"></a>
The column\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-dashboard-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FormatConfiguration`  <a name="cfn-quicksight-dashboard-columnconfiguration-formatconfiguration"></a>
The format configuration of a column\.  
*Required*: No  
*Type*: [FormatConfiguration](aws-properties-quicksight-dashboard-formatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Role`  <a name="cfn-quicksight-dashboard-columnconfiguration-role"></a>
The role of the column\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DIMENSION | MEASURE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)