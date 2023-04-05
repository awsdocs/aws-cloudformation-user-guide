# AWS::QuickSight::Template KPIOptions<a name="aws-properties-quicksight-template-kpioptions"></a>

The options that determine the presentation of a KPI visual\.

## Syntax<a name="aws-properties-quicksight-template-kpioptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-kpioptions-syntax.json"></a>

```
{
  "[Comparison](#cfn-quicksight-template-kpioptions-comparison)" : ComparisonConfiguration,
  "[PrimaryValueDisplayType](#cfn-quicksight-template-kpioptions-primaryvaluedisplaytype)" : String,
  "[PrimaryValueFontConfiguration](#cfn-quicksight-template-kpioptions-primaryvaluefontconfiguration)" : FontConfiguration,
  "[ProgressBar](#cfn-quicksight-template-kpioptions-progressbar)" : ProgressBarOptions,
  "[SecondaryValue](#cfn-quicksight-template-kpioptions-secondaryvalue)" : SecondaryValueOptions,
  "[SecondaryValueFontConfiguration](#cfn-quicksight-template-kpioptions-secondaryvaluefontconfiguration)" : FontConfiguration,
  "[TrendArrows](#cfn-quicksight-template-kpioptions-trendarrows)" : TrendArrowOptions
}
```

### YAML<a name="aws-properties-quicksight-template-kpioptions-syntax.yaml"></a>

```
  [Comparison](#cfn-quicksight-template-kpioptions-comparison): 
    ComparisonConfiguration
  [PrimaryValueDisplayType](#cfn-quicksight-template-kpioptions-primaryvaluedisplaytype): String
  [PrimaryValueFontConfiguration](#cfn-quicksight-template-kpioptions-primaryvaluefontconfiguration): 
    FontConfiguration
  [ProgressBar](#cfn-quicksight-template-kpioptions-progressbar): 
    ProgressBarOptions
  [SecondaryValue](#cfn-quicksight-template-kpioptions-secondaryvalue): 
    SecondaryValueOptions
  [SecondaryValueFontConfiguration](#cfn-quicksight-template-kpioptions-secondaryvaluefontconfiguration): 
    FontConfiguration
  [TrendArrows](#cfn-quicksight-template-kpioptions-trendarrows): 
    TrendArrowOptions
```

## Properties<a name="aws-properties-quicksight-template-kpioptions-properties"></a>

`Comparison`  <a name="cfn-quicksight-template-kpioptions-comparison"></a>
The comparison configuration of a KPI visual\.  
*Required*: No  
*Type*: [ComparisonConfiguration](aws-properties-quicksight-template-comparisonconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryValueDisplayType`  <a name="cfn-quicksight-template-kpioptions-primaryvaluedisplaytype"></a>
The options that determine the primary value display type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ACTUAL | COMPARISON | HIDDEN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryValueFontConfiguration`  <a name="cfn-quicksight-template-kpioptions-primaryvaluefontconfiguration"></a>
The options that determine the primary value font configuration\.  
*Required*: No  
*Type*: [FontConfiguration](aws-properties-quicksight-template-fontconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProgressBar`  <a name="cfn-quicksight-template-kpioptions-progressbar"></a>
The options that determine the presentation of the progress bar of a KPI visual\.  
*Required*: No  
*Type*: [ProgressBarOptions](aws-properties-quicksight-template-progressbaroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondaryValue`  <a name="cfn-quicksight-template-kpioptions-secondaryvalue"></a>
The options that determine the presentation of the secondary value of a KPI visual\.  
*Required*: No  
*Type*: [SecondaryValueOptions](aws-properties-quicksight-template-secondaryvalueoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondaryValueFontConfiguration`  <a name="cfn-quicksight-template-kpioptions-secondaryvaluefontconfiguration"></a>
The options that determine the secondary value font configuration\.  
*Required*: No  
*Type*: [FontConfiguration](aws-properties-quicksight-template-fontconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrendArrows`  <a name="cfn-quicksight-template-kpioptions-trendarrows"></a>
The options that determine the presentation of trend arrows in a KPI visual\.  
*Required*: No  
*Type*: [TrendArrowOptions](aws-properties-quicksight-template-trendarrowoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)