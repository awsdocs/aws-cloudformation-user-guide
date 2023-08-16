# AWS::QuickSight::Dashboard ForecastConfiguration<a name="aws-properties-quicksight-dashboard-forecastconfiguration"></a>

The forecast configuration that is used in a line chart's display properties\.

## Syntax<a name="aws-properties-quicksight-dashboard-forecastconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-forecastconfiguration-syntax.json"></a>

```
{
  "[ForecastProperties](#cfn-quicksight-dashboard-forecastconfiguration-forecastproperties)" : TimeBasedForecastProperties,
  "[Scenario](#cfn-quicksight-dashboard-forecastconfiguration-scenario)" : ForecastScenario
}
```

### YAML<a name="aws-properties-quicksight-dashboard-forecastconfiguration-syntax.yaml"></a>

```
  [ForecastProperties](#cfn-quicksight-dashboard-forecastconfiguration-forecastproperties): 
    TimeBasedForecastProperties
  [Scenario](#cfn-quicksight-dashboard-forecastconfiguration-scenario): 
    ForecastScenario
```

## Properties<a name="aws-properties-quicksight-dashboard-forecastconfiguration-properties"></a>

`ForecastProperties`  <a name="cfn-quicksight-dashboard-forecastconfiguration-forecastproperties"></a>
The forecast properties setup of a forecast in the line chart\.  
*Required*: No  
*Type*: [TimeBasedForecastProperties](aws-properties-quicksight-dashboard-timebasedforecastproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scenario`  <a name="cfn-quicksight-dashboard-forecastconfiguration-scenario"></a>
The forecast scenario of a forecast in the line chart\.  
*Required*: No  
*Type*: [ForecastScenario](aws-properties-quicksight-dashboard-forecastscenario.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)