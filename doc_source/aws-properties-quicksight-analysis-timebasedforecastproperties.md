# AWS::QuickSight::Analysis TimeBasedForecastProperties<a name="aws-properties-quicksight-analysis-timebasedforecastproperties"></a>

The forecast properties setup of a forecast in the line chart\.

## Syntax<a name="aws-properties-quicksight-analysis-timebasedforecastproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-timebasedforecastproperties-syntax.json"></a>

```
{
  "[LowerBoundary](#cfn-quicksight-analysis-timebasedforecastproperties-lowerboundary)" : Double,
  "[PeriodsBackward](#cfn-quicksight-analysis-timebasedforecastproperties-periodsbackward)" : Double,
  "[PeriodsForward](#cfn-quicksight-analysis-timebasedforecastproperties-periodsforward)" : Double,
  "[PredictionInterval](#cfn-quicksight-analysis-timebasedforecastproperties-predictioninterval)" : Double,
  "[Seasonality](#cfn-quicksight-analysis-timebasedforecastproperties-seasonality)" : Double,
  "[UpperBoundary](#cfn-quicksight-analysis-timebasedforecastproperties-upperboundary)" : Double
}
```

### YAML<a name="aws-properties-quicksight-analysis-timebasedforecastproperties-syntax.yaml"></a>

```
  [LowerBoundary](#cfn-quicksight-analysis-timebasedforecastproperties-lowerboundary): Double
  [PeriodsBackward](#cfn-quicksight-analysis-timebasedforecastproperties-periodsbackward): Double
  [PeriodsForward](#cfn-quicksight-analysis-timebasedforecastproperties-periodsforward): Double
  [PredictionInterval](#cfn-quicksight-analysis-timebasedforecastproperties-predictioninterval): Double
  [Seasonality](#cfn-quicksight-analysis-timebasedforecastproperties-seasonality): Double
  [UpperBoundary](#cfn-quicksight-analysis-timebasedforecastproperties-upperboundary): Double
```

## Properties<a name="aws-properties-quicksight-analysis-timebasedforecastproperties-properties"></a>

`LowerBoundary`  <a name="cfn-quicksight-analysis-timebasedforecastproperties-lowerboundary"></a>
The lower boundary setup of a forecast computation\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PeriodsBackward`  <a name="cfn-quicksight-analysis-timebasedforecastproperties-periodsbackward"></a>
The periods backward setup of a forecast computation\.  
*Required*: No  
*Type*: Double  
*Minimum*: `0`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PeriodsForward`  <a name="cfn-quicksight-analysis-timebasedforecastproperties-periodsforward"></a>
The periods forward setup of a forecast computation\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PredictionInterval`  <a name="cfn-quicksight-analysis-timebasedforecastproperties-predictioninterval"></a>
The prediction interval setup of a forecast computation\.  
*Required*: No  
*Type*: Double  
*Minimum*: `50`  
*Maximum*: `95`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Seasonality`  <a name="cfn-quicksight-analysis-timebasedforecastproperties-seasonality"></a>
The seasonality setup of a forecast computation\. Choose one of the following options:  
+  `NULL`: The input is set to `NULL`\.
+  `NON_NULL`: The input is set to a custom value\.
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `180`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpperBoundary`  <a name="cfn-quicksight-analysis-timebasedforecastproperties-upperboundary"></a>
The upper boundary setup of a forecast computation\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)