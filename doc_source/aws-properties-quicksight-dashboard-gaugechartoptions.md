# AWS::QuickSight::Dashboard GaugeChartOptions<a name="aws-properties-quicksight-dashboard-gaugechartoptions"></a>

The options that determine the presentation of the `GaugeChartVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-gaugechartoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-gaugechartoptions-syntax.json"></a>

```
{
  "[Arc](#cfn-quicksight-dashboard-gaugechartoptions-arc)" : ArcConfiguration,
  "[ArcAxis](#cfn-quicksight-dashboard-gaugechartoptions-arcaxis)" : ArcAxisConfiguration,
  "[Comparison](#cfn-quicksight-dashboard-gaugechartoptions-comparison)" : ComparisonConfiguration,
  "[PrimaryValueDisplayType](#cfn-quicksight-dashboard-gaugechartoptions-primaryvaluedisplaytype)" : String,
  "[PrimaryValueFontConfiguration](#cfn-quicksight-dashboard-gaugechartoptions-primaryvaluefontconfiguration)" : FontConfiguration
}
```

### YAML<a name="aws-properties-quicksight-dashboard-gaugechartoptions-syntax.yaml"></a>

```
  [Arc](#cfn-quicksight-dashboard-gaugechartoptions-arc): 
    ArcConfiguration
  [ArcAxis](#cfn-quicksight-dashboard-gaugechartoptions-arcaxis): 
    ArcAxisConfiguration
  [Comparison](#cfn-quicksight-dashboard-gaugechartoptions-comparison): 
    ComparisonConfiguration
  [PrimaryValueDisplayType](#cfn-quicksight-dashboard-gaugechartoptions-primaryvaluedisplaytype): String
  [PrimaryValueFontConfiguration](#cfn-quicksight-dashboard-gaugechartoptions-primaryvaluefontconfiguration): 
    FontConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-gaugechartoptions-properties"></a>

`Arc`  <a name="cfn-quicksight-dashboard-gaugechartoptions-arc"></a>
The arc configuration of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: [ArcConfiguration](aws-properties-quicksight-dashboard-arcconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ArcAxis`  <a name="cfn-quicksight-dashboard-gaugechartoptions-arcaxis"></a>
The arc axis configuration of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: [ArcAxisConfiguration](aws-properties-quicksight-dashboard-arcaxisconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Comparison`  <a name="cfn-quicksight-dashboard-gaugechartoptions-comparison"></a>
The comparison configuration of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: [ComparisonConfiguration](aws-properties-quicksight-dashboard-comparisonconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryValueDisplayType`  <a name="cfn-quicksight-dashboard-gaugechartoptions-primaryvaluedisplaytype"></a>
The options that determine the primary value display type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ACTUAL | COMPARISON | HIDDEN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryValueFontConfiguration`  <a name="cfn-quicksight-dashboard-gaugechartoptions-primaryvaluefontconfiguration"></a>
The options that determine the primary value font configuration\.  
*Required*: No  
*Type*: [FontConfiguration](aws-properties-quicksight-dashboard-fontconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)