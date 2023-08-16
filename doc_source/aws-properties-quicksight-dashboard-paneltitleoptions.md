# AWS::QuickSight::Dashboard PanelTitleOptions<a name="aws-properties-quicksight-dashboard-paneltitleoptions"></a>

The options that determine the title styles for each small multiples panel\.

## Syntax<a name="aws-properties-quicksight-dashboard-paneltitleoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-paneltitleoptions-syntax.json"></a>

```
{
  "[FontConfiguration](#cfn-quicksight-dashboard-paneltitleoptions-fontconfiguration)" : FontConfiguration,
  "[HorizontalTextAlignment](#cfn-quicksight-dashboard-paneltitleoptions-horizontaltextalignment)" : String,
  "[Visibility](#cfn-quicksight-dashboard-paneltitleoptions-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-paneltitleoptions-syntax.yaml"></a>

```
  [FontConfiguration](#cfn-quicksight-dashboard-paneltitleoptions-fontconfiguration): 
    FontConfiguration
  [HorizontalTextAlignment](#cfn-quicksight-dashboard-paneltitleoptions-horizontaltextalignment): String
  [Visibility](#cfn-quicksight-dashboard-paneltitleoptions-visibility): String
```

## Properties<a name="aws-properties-quicksight-dashboard-paneltitleoptions-properties"></a>

`FontConfiguration`  <a name="cfn-quicksight-dashboard-paneltitleoptions-fontconfiguration"></a>
Property description not available\.  
*Required*: No  
*Type*: [FontConfiguration](aws-properties-quicksight-dashboard-fontconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HorizontalTextAlignment`  <a name="cfn-quicksight-dashboard-paneltitleoptions-horizontaltextalignment"></a>
Sets the horizontal text alignment of the title within each panel\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTO | CENTER | LEFT | RIGHT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-dashboard-paneltitleoptions-visibility"></a>
Determines whether or not panel titles are displayed\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)