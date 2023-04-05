# AWS::QuickSight::Dashboard ArcAxisConfiguration<a name="aws-properties-quicksight-dashboard-arcaxisconfiguration"></a>

The arc axis configuration of a `GaugeChartVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-arcaxisconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-arcaxisconfiguration-syntax.json"></a>

```
{
  "[Range](#cfn-quicksight-dashboard-arcaxisconfiguration-range)" : ArcAxisDisplayRange,
  "[ReserveRange](#cfn-quicksight-dashboard-arcaxisconfiguration-reserverange)" : Double
}
```

### YAML<a name="aws-properties-quicksight-dashboard-arcaxisconfiguration-syntax.yaml"></a>

```
  [Range](#cfn-quicksight-dashboard-arcaxisconfiguration-range): 
    ArcAxisDisplayRange
  [ReserveRange](#cfn-quicksight-dashboard-arcaxisconfiguration-reserverange): Double
```

## Properties<a name="aws-properties-quicksight-dashboard-arcaxisconfiguration-properties"></a>

`Range`  <a name="cfn-quicksight-dashboard-arcaxisconfiguration-range"></a>
The arc axis range of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: [ArcAxisDisplayRange](aws-properties-quicksight-dashboard-arcaxisdisplayrange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReserveRange`  <a name="cfn-quicksight-dashboard-arcaxisconfiguration-reserverange"></a>
The reserved range of the arc axis\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)