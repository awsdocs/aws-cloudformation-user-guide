# AWS::QuickSight::Dashboard LegendOptions<a name="aws-properties-quicksight-dashboard-legendoptions"></a>

The options for the legend setup of a visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-legendoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-legendoptions-syntax.json"></a>

```
{
  "[Height](#cfn-quicksight-dashboard-legendoptions-height)" : String,
  "[Position](#cfn-quicksight-dashboard-legendoptions-position)" : String,
  "[Title](#cfn-quicksight-dashboard-legendoptions-title)" : LabelOptions,
  "[Visibility](#cfn-quicksight-dashboard-legendoptions-visibility)" : String,
  "[Width](#cfn-quicksight-dashboard-legendoptions-width)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-legendoptions-syntax.yaml"></a>

```
  [Height](#cfn-quicksight-dashboard-legendoptions-height): String
  [Position](#cfn-quicksight-dashboard-legendoptions-position): String
  [Title](#cfn-quicksight-dashboard-legendoptions-title): 
    LabelOptions
  [Visibility](#cfn-quicksight-dashboard-legendoptions-visibility): String
  [Width](#cfn-quicksight-dashboard-legendoptions-width): String
```

## Properties<a name="aws-properties-quicksight-dashboard-legendoptions-properties"></a>

`Height`  <a name="cfn-quicksight-dashboard-legendoptions-height"></a>
The height of the legend\. If this value is omitted, a default height is used when rendering\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Position`  <a name="cfn-quicksight-dashboard-legendoptions-position"></a>
The positions for the legend\. Choose one of the following options:  
+  `AUTO` 
+  `RIGHT` 
+  `BOTTOM` 
+  `LEFT` 
*Required*: No  
*Type*: String  
*Allowed values*: `AUTO | BOTTOM | RIGHT | TOP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-legendoptions-title"></a>
The custom title for the legend\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-dashboard-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-dashboard-legendoptions-visibility"></a>
Determines whether or not the legend is visible\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Width`  <a name="cfn-quicksight-dashboard-legendoptions-width"></a>
The width of the legend\. If this value is omitted, a default width is used when rendering\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)