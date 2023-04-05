# AWS::QuickSight::Analysis BoxPlotOptions<a name="aws-properties-quicksight-analysis-boxplotoptions"></a>

The options of a box plot visual\.

## Syntax<a name="aws-properties-quicksight-analysis-boxplotoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-boxplotoptions-syntax.json"></a>

```
{
  "[AllDataPointsVisibility](#cfn-quicksight-analysis-boxplotoptions-alldatapointsvisibility)" : String,
  "[OutlierVisibility](#cfn-quicksight-analysis-boxplotoptions-outliervisibility)" : String,
  "[StyleOptions](#cfn-quicksight-analysis-boxplotoptions-styleoptions)" : BoxPlotStyleOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-boxplotoptions-syntax.yaml"></a>

```
  [AllDataPointsVisibility](#cfn-quicksight-analysis-boxplotoptions-alldatapointsvisibility): String
  [OutlierVisibility](#cfn-quicksight-analysis-boxplotoptions-outliervisibility): String
  [StyleOptions](#cfn-quicksight-analysis-boxplotoptions-styleoptions): 
    BoxPlotStyleOptions
```

## Properties<a name="aws-properties-quicksight-analysis-boxplotoptions-properties"></a>

`AllDataPointsVisibility`  <a name="cfn-quicksight-analysis-boxplotoptions-alldatapointsvisibility"></a>
Determines the visibility of all data points of the box plot\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutlierVisibility`  <a name="cfn-quicksight-analysis-boxplotoptions-outliervisibility"></a>
Determines the visibility of the outlier in a box plot\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StyleOptions`  <a name="cfn-quicksight-analysis-boxplotoptions-styleoptions"></a>
The style options of the box plot\.  
*Required*: No  
*Type*: [BoxPlotStyleOptions](aws-properties-quicksight-analysis-boxplotstyleoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)