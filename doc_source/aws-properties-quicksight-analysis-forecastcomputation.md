# AWS::QuickSight::Analysis ForecastComputation<a name="aws-properties-quicksight-analysis-forecastcomputation"></a>

The forecast computation configuration\.

## Syntax<a name="aws-properties-quicksight-analysis-forecastcomputation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-forecastcomputation-syntax.json"></a>

```
{
  "[ComputationId](#cfn-quicksight-analysis-forecastcomputation-computationid)" : String,
  "[CustomSeasonalityValue](#cfn-quicksight-analysis-forecastcomputation-customseasonalityvalue)" : Double,
  "[LowerBoundary](#cfn-quicksight-analysis-forecastcomputation-lowerboundary)" : Double,
  "[Name](#cfn-quicksight-analysis-forecastcomputation-name)" : String,
  "[PeriodsBackward](#cfn-quicksight-analysis-forecastcomputation-periodsbackward)" : Double,
  "[PeriodsForward](#cfn-quicksight-analysis-forecastcomputation-periodsforward)" : Double,
  "[PredictionInterval](#cfn-quicksight-analysis-forecastcomputation-predictioninterval)" : Double,
  "[Seasonality](#cfn-quicksight-analysis-forecastcomputation-seasonality)" : String,
  "[Time](#cfn-quicksight-analysis-forecastcomputation-time)" : DimensionField,
  "[UpperBoundary](#cfn-quicksight-analysis-forecastcomputation-upperboundary)" : Double,
  "[Value](#cfn-quicksight-analysis-forecastcomputation-value)" : MeasureField
}
```

### YAML<a name="aws-properties-quicksight-analysis-forecastcomputation-syntax.yaml"></a>

```
  [ComputationId](#cfn-quicksight-analysis-forecastcomputation-computationid): String
  [CustomSeasonalityValue](#cfn-quicksight-analysis-forecastcomputation-customseasonalityvalue): Double
  [LowerBoundary](#cfn-quicksight-analysis-forecastcomputation-lowerboundary): Double
  [Name](#cfn-quicksight-analysis-forecastcomputation-name): String
  [PeriodsBackward](#cfn-quicksight-analysis-forecastcomputation-periodsbackward): Double
  [PeriodsForward](#cfn-quicksight-analysis-forecastcomputation-periodsforward): Double
  [PredictionInterval](#cfn-quicksight-analysis-forecastcomputation-predictioninterval): Double
  [Seasonality](#cfn-quicksight-analysis-forecastcomputation-seasonality): String
  [Time](#cfn-quicksight-analysis-forecastcomputation-time): 
    DimensionField
  [UpperBoundary](#cfn-quicksight-analysis-forecastcomputation-upperboundary): Double
  [Value](#cfn-quicksight-analysis-forecastcomputation-value): 
    MeasureField
```

## Properties<a name="aws-properties-quicksight-analysis-forecastcomputation-properties"></a>

`ComputationId`  <a name="cfn-quicksight-analysis-forecastcomputation-computationid"></a>
The ID for a computation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomSeasonalityValue`  <a name="cfn-quicksight-analysis-forecastcomputation-customseasonalityvalue"></a>
The custom seasonality value setup of a forecast computation\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `180`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LowerBoundary`  <a name="cfn-quicksight-analysis-forecastcomputation-lowerboundary"></a>
The lower boundary setup of a forecast computation\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-analysis-forecastcomputation-name"></a>
The name of a computation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PeriodsBackward`  <a name="cfn-quicksight-analysis-forecastcomputation-periodsbackward"></a>
The periods backward setup of a forecast computation\.  
*Required*: No  
*Type*: Double  
*Minimum*: `0`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PeriodsForward`  <a name="cfn-quicksight-analysis-forecastcomputation-periodsforward"></a>
The periods forward setup of a forecast computation\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PredictionInterval`  <a name="cfn-quicksight-analysis-forecastcomputation-predictioninterval"></a>
The prediction interval setup of a forecast computation\.  
*Required*: No  
*Type*: Double  
*Minimum*: `50`  
*Maximum*: `95`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Seasonality`  <a name="cfn-quicksight-analysis-forecastcomputation-seasonality"></a>
The seasonality setup of a forecast computation\. Choose one of the following options:  
+  `AUTOMATIC` 
+  `CUSTOM`: Checks the custom seasonality value\.
*Required*: No  
*Type*: String  
*Allowed values*: `AUTOMATIC | CUSTOM`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Time`  <a name="cfn-quicksight-analysis-forecastcomputation-time"></a>
The time field that is used in a computation\.  
*Required*: No  
*Type*: [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpperBoundary`  <a name="cfn-quicksight-analysis-forecastcomputation-upperboundary"></a>
The upper boundary setup of a forecast computation\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-analysis-forecastcomputation-value"></a>
The value field that is used in a computation\.  
*Required*: No  
*Type*: [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)