# AWS::QuickSight::Dashboard FieldTooltipItem<a name="aws-properties-quicksight-dashboard-fieldtooltipitem"></a>

The tooltip item for the fields\.

## Syntax<a name="aws-properties-quicksight-dashboard-fieldtooltipitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-fieldtooltipitem-syntax.json"></a>

```
{
  "[FieldId](#cfn-quicksight-dashboard-fieldtooltipitem-fieldid)" : String,
  "[Label](#cfn-quicksight-dashboard-fieldtooltipitem-label)" : String,
  "[Visibility](#cfn-quicksight-dashboard-fieldtooltipitem-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-fieldtooltipitem-syntax.yaml"></a>

```
  [FieldId](#cfn-quicksight-dashboard-fieldtooltipitem-fieldid): String
  [Label](#cfn-quicksight-dashboard-fieldtooltipitem-label): String
  [Visibility](#cfn-quicksight-dashboard-fieldtooltipitem-visibility): String
```

## Properties<a name="aws-properties-quicksight-dashboard-fieldtooltipitem-properties"></a>

`FieldId`  <a name="cfn-quicksight-dashboard-fieldtooltipitem-fieldid"></a>
The unique ID of the field that is targeted by the tooltip\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Label`  <a name="cfn-quicksight-dashboard-fieldtooltipitem-label"></a>
The label of the tooltip item\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-dashboard-fieldtooltipitem-visibility"></a>
The visibility of the tooltip item\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)