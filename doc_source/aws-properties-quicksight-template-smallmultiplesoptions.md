# AWS::QuickSight::Template SmallMultiplesOptions<a name="aws-properties-quicksight-template-smallmultiplesoptions"></a>

Options that determine the layout and display options of a chart's small multiples\.

## Syntax<a name="aws-properties-quicksight-template-smallmultiplesoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-smallmultiplesoptions-syntax.json"></a>

```
{
  "[MaxVisibleColumns](#cfn-quicksight-template-smallmultiplesoptions-maxvisiblecolumns)" : Double,
  "[MaxVisibleRows](#cfn-quicksight-template-smallmultiplesoptions-maxvisiblerows)" : Double,
  "[PanelConfiguration](#cfn-quicksight-template-smallmultiplesoptions-panelconfiguration)" : PanelConfiguration,
  "[XAxis](#cfn-quicksight-template-smallmultiplesoptions-xaxis)" : SmallMultiplesAxisProperties,
  "[YAxis](#cfn-quicksight-template-smallmultiplesoptions-yaxis)" : SmallMultiplesAxisProperties
}
```

### YAML<a name="aws-properties-quicksight-template-smallmultiplesoptions-syntax.yaml"></a>

```
  [MaxVisibleColumns](#cfn-quicksight-template-smallmultiplesoptions-maxvisiblecolumns): Double
  [MaxVisibleRows](#cfn-quicksight-template-smallmultiplesoptions-maxvisiblerows): Double
  [PanelConfiguration](#cfn-quicksight-template-smallmultiplesoptions-panelconfiguration): 
    PanelConfiguration
  [XAxis](#cfn-quicksight-template-smallmultiplesoptions-xaxis): 
    SmallMultiplesAxisProperties
  [YAxis](#cfn-quicksight-template-smallmultiplesoptions-yaxis): 
    SmallMultiplesAxisProperties
```

## Properties<a name="aws-properties-quicksight-template-smallmultiplesoptions-properties"></a>

`MaxVisibleColumns`  <a name="cfn-quicksight-template-smallmultiplesoptions-maxvisiblecolumns"></a>
Sets the maximum number of visible columns to display in the grid of small multiples panels\.  
The default is `Auto`, which automatically adjusts the columns in the grid to fit the overall layout and size of the given chart\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxVisibleRows`  <a name="cfn-quicksight-template-smallmultiplesoptions-maxvisiblerows"></a>
Sets the maximum number of visible rows to display in the grid of small multiples panels\.  
The default value is `Auto`, which automatically adjusts the rows in the grid to fit the overall layout and size of the given chart\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PanelConfiguration`  <a name="cfn-quicksight-template-smallmultiplesoptions-panelconfiguration"></a>
Configures the display options for each small multiples panel\.  
*Required*: No  
*Type*: [PanelConfiguration](aws-properties-quicksight-template-panelconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XAxis`  <a name="cfn-quicksight-template-smallmultiplesoptions-xaxis"></a>
The properties of a small multiples X axis\.  
*Required*: No  
*Type*: [SmallMultiplesAxisProperties](aws-properties-quicksight-template-smallmultiplesaxisproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`YAxis`  <a name="cfn-quicksight-template-smallmultiplesoptions-yaxis"></a>
The properties of a small multiples Y axis\.  
*Required*: No  
*Type*: [SmallMultiplesAxisProperties](aws-properties-quicksight-template-smallmultiplesaxisproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)