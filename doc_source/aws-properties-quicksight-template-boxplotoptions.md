# AWS::QuickSight::Template BoxPlotOptions<a name="aws-properties-quicksight-template-boxplotoptions"></a>

The options of a box plot visual\.

## Syntax<a name="aws-properties-quicksight-template-boxplotoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-boxplotoptions-syntax.json"></a>

```
{
  "[AllDataPointsVisibility](#cfn-quicksight-template-boxplotoptions-alldatapointsvisibility)" : String,
  "[OutlierVisibility](#cfn-quicksight-template-boxplotoptions-outliervisibility)" : String,
  "[StyleOptions](#cfn-quicksight-template-boxplotoptions-styleoptions)" : BoxPlotStyleOptions
}
```

### YAML<a name="aws-properties-quicksight-template-boxplotoptions-syntax.yaml"></a>

```
  [AllDataPointsVisibility](#cfn-quicksight-template-boxplotoptions-alldatapointsvisibility): String
  [OutlierVisibility](#cfn-quicksight-template-boxplotoptions-outliervisibility): String
  [StyleOptions](#cfn-quicksight-template-boxplotoptions-styleoptions): 
    BoxPlotStyleOptions
```

## Properties<a name="aws-properties-quicksight-template-boxplotoptions-properties"></a>

`AllDataPointsVisibility`  <a name="cfn-quicksight-template-boxplotoptions-alldatapointsvisibility"></a>
Determines the visibility of all data points of the box plot\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutlierVisibility`  <a name="cfn-quicksight-template-boxplotoptions-outliervisibility"></a>
Determines the visibility of the outlier in a box plot\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StyleOptions`  <a name="cfn-quicksight-template-boxplotoptions-styleoptions"></a>
The style options of the box plot\.  
*Required*: No  
*Type*: [BoxPlotStyleOptions](aws-properties-quicksight-template-boxplotstyleoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)