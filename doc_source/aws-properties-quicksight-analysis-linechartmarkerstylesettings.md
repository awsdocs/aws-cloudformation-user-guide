# AWS::QuickSight::Analysis LineChartMarkerStyleSettings<a name="aws-properties-quicksight-analysis-linechartmarkerstylesettings"></a>

Marker styles options for a line series in `LineChartVisual`\.

## Syntax<a name="aws-properties-quicksight-analysis-linechartmarkerstylesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-linechartmarkerstylesettings-syntax.json"></a>

```
{
  "[MarkerColor](#cfn-quicksight-analysis-linechartmarkerstylesettings-markercolor)" : String,
  "[MarkerShape](#cfn-quicksight-analysis-linechartmarkerstylesettings-markershape)" : String,
  "[MarkerSize](#cfn-quicksight-analysis-linechartmarkerstylesettings-markersize)" : String,
  "[MarkerVisibility](#cfn-quicksight-analysis-linechartmarkerstylesettings-markervisibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-linechartmarkerstylesettings-syntax.yaml"></a>

```
  [MarkerColor](#cfn-quicksight-analysis-linechartmarkerstylesettings-markercolor): String
  [MarkerShape](#cfn-quicksight-analysis-linechartmarkerstylesettings-markershape): String
  [MarkerSize](#cfn-quicksight-analysis-linechartmarkerstylesettings-markersize): String
  [MarkerVisibility](#cfn-quicksight-analysis-linechartmarkerstylesettings-markervisibility): String
```

## Properties<a name="aws-properties-quicksight-analysis-linechartmarkerstylesettings-properties"></a>

`MarkerColor`  <a name="cfn-quicksight-analysis-linechartmarkerstylesettings-markercolor"></a>
Color of marker in the series\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MarkerShape`  <a name="cfn-quicksight-analysis-linechartmarkerstylesettings-markershape"></a>
Shape option for markers in the series\.  
+  `CIRCLE`: Show marker as a circle\.
+  `TRIANGLE`: Show marker as a triangle\.
+  `SQUARE`: Show marker as a square\.
+  `DIAMOND`: Show marker as a diamond\.
+  `ROUNDED_SQUARE`: Show marker as a rounded square\.
*Required*: No  
*Type*: String  
*Allowed values*: `CIRCLE | DIAMOND | ROUNDED_SQUARE | SQUARE | TRIANGLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MarkerSize`  <a name="cfn-quicksight-analysis-linechartmarkerstylesettings-markersize"></a>
Size of marker in the series\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MarkerVisibility`  <a name="cfn-quicksight-analysis-linechartmarkerstylesettings-markervisibility"></a>
Configuration option that determines whether to show the markers in the series\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)