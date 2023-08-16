# AWS::QuickSight::Dashboard LineChartLineStyleSettings<a name="aws-properties-quicksight-dashboard-linechartlinestylesettings"></a>

Line styles options for a line series in `LineChartVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-linechartlinestylesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-linechartlinestylesettings-syntax.json"></a>

```
{
  "[LineInterpolation](#cfn-quicksight-dashboard-linechartlinestylesettings-lineinterpolation)" : String,
  "[LineStyle](#cfn-quicksight-dashboard-linechartlinestylesettings-linestyle)" : String,
  "[LineVisibility](#cfn-quicksight-dashboard-linechartlinestylesettings-linevisibility)" : String,
  "[LineWidth](#cfn-quicksight-dashboard-linechartlinestylesettings-linewidth)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-linechartlinestylesettings-syntax.yaml"></a>

```
  [LineInterpolation](#cfn-quicksight-dashboard-linechartlinestylesettings-lineinterpolation): String
  [LineStyle](#cfn-quicksight-dashboard-linechartlinestylesettings-linestyle): String
  [LineVisibility](#cfn-quicksight-dashboard-linechartlinestylesettings-linevisibility): String
  [LineWidth](#cfn-quicksight-dashboard-linechartlinestylesettings-linewidth): String
```

## Properties<a name="aws-properties-quicksight-dashboard-linechartlinestylesettings-properties"></a>

`LineInterpolation`  <a name="cfn-quicksight-dashboard-linechartlinestylesettings-lineinterpolation"></a>
Interpolation style for line series\.  
+  `LINEAR`: Show as default, linear style\.
+  `SMOOTH`: Show as a smooth curve\.
+  `STEPPED`: Show steps in line\.
*Required*: No  
*Type*: String  
*Allowed values*: `LINEAR | SMOOTH | STEPPED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LineStyle`  <a name="cfn-quicksight-dashboard-linechartlinestylesettings-linestyle"></a>
Line style for line series\.  
+  `SOLID`: Show as a solid line\.
+  `DOTTED`: Show as a dotted line\.
+  `DASHED`: Show as a dashed line\.
*Required*: No  
*Type*: String  
*Allowed values*: `DASHED | DOTTED | SOLID`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LineVisibility`  <a name="cfn-quicksight-dashboard-linechartlinestylesettings-linevisibility"></a>
Configuration option that determines whether to show the line for the series\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LineWidth`  <a name="cfn-quicksight-dashboard-linechartlinestylesettings-linewidth"></a>
Width that determines the line thickness\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)