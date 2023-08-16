# AWS::QuickSight::Analysis TooltipOptions<a name="aws-properties-quicksight-analysis-tooltipoptions"></a>

The display options for the visual tooltip\.

## Syntax<a name="aws-properties-quicksight-analysis-tooltipoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-tooltipoptions-syntax.json"></a>

```
{
  "[FieldBasedTooltip](#cfn-quicksight-analysis-tooltipoptions-fieldbasedtooltip)" : FieldBasedTooltip,
  "[SelectedTooltipType](#cfn-quicksight-analysis-tooltipoptions-selectedtooltiptype)" : String,
  "[TooltipVisibility](#cfn-quicksight-analysis-tooltipoptions-tooltipvisibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-tooltipoptions-syntax.yaml"></a>

```
  [FieldBasedTooltip](#cfn-quicksight-analysis-tooltipoptions-fieldbasedtooltip): 
    FieldBasedTooltip
  [SelectedTooltipType](#cfn-quicksight-analysis-tooltipoptions-selectedtooltiptype): String
  [TooltipVisibility](#cfn-quicksight-analysis-tooltipoptions-tooltipvisibility): String
```

## Properties<a name="aws-properties-quicksight-analysis-tooltipoptions-properties"></a>

`FieldBasedTooltip`  <a name="cfn-quicksight-analysis-tooltipoptions-fieldbasedtooltip"></a>
The setup for the detailed tooltip\. The tooltip setup is always saved\. The display type is decided based on the tooltip type\.  
*Required*: No  
*Type*: [FieldBasedTooltip](aws-properties-quicksight-analysis-fieldbasedtooltip.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectedTooltipType`  <a name="cfn-quicksight-analysis-tooltipoptions-selectedtooltiptype"></a>
The selected type for the tooltip\. Choose one of the following options:  
+  `BASIC`: A basic tooltip\.
+  `DETAILED`: A detailed tooltip\.
*Required*: No  
*Type*: String  
*Allowed values*: `BASIC | DETAILED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TooltipVisibility`  <a name="cfn-quicksight-analysis-tooltipoptions-tooltipvisibility"></a>
Determines whether or not the tooltip is visible\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)