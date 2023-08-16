# AWS::QuickSight::Dashboard TableRowConditionalFormatting<a name="aws-properties-quicksight-dashboard-tablerowconditionalformatting"></a>

The conditional formatting of a table row\.

## Syntax<a name="aws-properties-quicksight-dashboard-tablerowconditionalformatting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-tablerowconditionalformatting-syntax.json"></a>

```
{
  "[BackgroundColor](#cfn-quicksight-dashboard-tablerowconditionalformatting-backgroundcolor)" : ConditionalFormattingColor,
  "[TextColor](#cfn-quicksight-dashboard-tablerowconditionalformatting-textcolor)" : ConditionalFormattingColor
}
```

### YAML<a name="aws-properties-quicksight-dashboard-tablerowconditionalformatting-syntax.yaml"></a>

```
  [BackgroundColor](#cfn-quicksight-dashboard-tablerowconditionalformatting-backgroundcolor): 
    ConditionalFormattingColor
  [TextColor](#cfn-quicksight-dashboard-tablerowconditionalformatting-textcolor): 
    ConditionalFormattingColor
```

## Properties<a name="aws-properties-quicksight-dashboard-tablerowconditionalformatting-properties"></a>

`BackgroundColor`  <a name="cfn-quicksight-dashboard-tablerowconditionalformatting-backgroundcolor"></a>
The conditional formatting color \(solid, gradient\) of the background for a table row\.  
*Required*: No  
*Type*: [ConditionalFormattingColor](aws-properties-quicksight-dashboard-conditionalformattingcolor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextColor`  <a name="cfn-quicksight-dashboard-tablerowconditionalformatting-textcolor"></a>
The conditional formatting color \(solid, gradient\) of the text for a table row\.  
*Required*: No  
*Type*: [ConditionalFormattingColor](aws-properties-quicksight-dashboard-conditionalformattingcolor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)