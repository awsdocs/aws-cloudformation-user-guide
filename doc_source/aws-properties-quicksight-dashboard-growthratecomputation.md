# AWS::QuickSight::Dashboard GrowthRateComputation<a name="aws-properties-quicksight-dashboard-growthratecomputation"></a>

The growth rate computation configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-growthratecomputation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-growthratecomputation-syntax.json"></a>

```
{
  "[ComputationId](#cfn-quicksight-dashboard-growthratecomputation-computationid)" : String,
  "[Name](#cfn-quicksight-dashboard-growthratecomputation-name)" : String,
  "[PeriodSize](#cfn-quicksight-dashboard-growthratecomputation-periodsize)" : Double,
  "[Time](#cfn-quicksight-dashboard-growthratecomputation-time)" : DimensionField,
  "[Value](#cfn-quicksight-dashboard-growthratecomputation-value)" : MeasureField
}
```

### YAML<a name="aws-properties-quicksight-dashboard-growthratecomputation-syntax.yaml"></a>

```
  [ComputationId](#cfn-quicksight-dashboard-growthratecomputation-computationid): String
  [Name](#cfn-quicksight-dashboard-growthratecomputation-name): String
  [PeriodSize](#cfn-quicksight-dashboard-growthratecomputation-periodsize): Double
  [Time](#cfn-quicksight-dashboard-growthratecomputation-time): 
    DimensionField
  [Value](#cfn-quicksight-dashboard-growthratecomputation-value): 
    MeasureField
```

## Properties<a name="aws-properties-quicksight-dashboard-growthratecomputation-properties"></a>

`ComputationId`  <a name="cfn-quicksight-dashboard-growthratecomputation-computationid"></a>
The ID for a computation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-dashboard-growthratecomputation-name"></a>
The name of a computation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PeriodSize`  <a name="cfn-quicksight-dashboard-growthratecomputation-periodsize"></a>
The period size setup of a growth rate computation\.  
*Required*: No  
*Type*: Double  
*Minimum*: `2`  
*Maximum*: `52`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Time`  <a name="cfn-quicksight-dashboard-growthratecomputation-time"></a>
The time field that is used in a computation\.  
*Required*: Yes  
*Type*: [DimensionField](aws-properties-quicksight-dashboard-dimensionfield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-dashboard-growthratecomputation-value"></a>
The value field that is used in a computation\.  
*Required*: No  
*Type*: [MeasureField](aws-properties-quicksight-dashboard-measurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)