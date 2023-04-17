# AWS::QuickSight::Template GaugeChartOptions<a name="aws-properties-quicksight-template-gaugechartoptions"></a>

The options that determine the presentation of the `GaugeChartVisual`\.

## Syntax<a name="aws-properties-quicksight-template-gaugechartoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-gaugechartoptions-syntax.json"></a>

```
{
  "[Arc](#cfn-quicksight-template-gaugechartoptions-arc)" : ArcConfiguration,
  "[ArcAxis](#cfn-quicksight-template-gaugechartoptions-arcaxis)" : ArcAxisConfiguration,
  "[Comparison](#cfn-quicksight-template-gaugechartoptions-comparison)" : ComparisonConfiguration,
  "[PrimaryValueDisplayType](#cfn-quicksight-template-gaugechartoptions-primaryvaluedisplaytype)" : String,
  "[PrimaryValueFontConfiguration](#cfn-quicksight-template-gaugechartoptions-primaryvaluefontconfiguration)" : FontConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-gaugechartoptions-syntax.yaml"></a>

```
  [Arc](#cfn-quicksight-template-gaugechartoptions-arc): 
    ArcConfiguration
  [ArcAxis](#cfn-quicksight-template-gaugechartoptions-arcaxis): 
    ArcAxisConfiguration
  [Comparison](#cfn-quicksight-template-gaugechartoptions-comparison): 
    ComparisonConfiguration
  [PrimaryValueDisplayType](#cfn-quicksight-template-gaugechartoptions-primaryvaluedisplaytype): String
  [PrimaryValueFontConfiguration](#cfn-quicksight-template-gaugechartoptions-primaryvaluefontconfiguration): 
    FontConfiguration
```

## Properties<a name="aws-properties-quicksight-template-gaugechartoptions-properties"></a>

`Arc`  <a name="cfn-quicksight-template-gaugechartoptions-arc"></a>
The arc configuration of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: [ArcConfiguration](aws-properties-quicksight-template-arcconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ArcAxis`  <a name="cfn-quicksight-template-gaugechartoptions-arcaxis"></a>
The arc axis configuration of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: [ArcAxisConfiguration](aws-properties-quicksight-template-arcaxisconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Comparison`  <a name="cfn-quicksight-template-gaugechartoptions-comparison"></a>
The comparison configuration of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: [ComparisonConfiguration](aws-properties-quicksight-template-comparisonconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryValueDisplayType`  <a name="cfn-quicksight-template-gaugechartoptions-primaryvaluedisplaytype"></a>
The options that determine the primary value display type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ACTUAL | COMPARISON | HIDDEN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryValueFontConfiguration`  <a name="cfn-quicksight-template-gaugechartoptions-primaryvaluefontconfiguration"></a>
The options that determine the primary value font configuration\.  
*Required*: No  
*Type*: [FontConfiguration](aws-properties-quicksight-template-fontconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)