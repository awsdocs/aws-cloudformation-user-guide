# AWS::QuickSight::Dashboard ForecastScenario<a name="aws-properties-quicksight-dashboard-forecastscenario"></a>

The forecast scenario of a forecast in the line chart\.

## Syntax<a name="aws-properties-quicksight-dashboard-forecastscenario-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-forecastscenario-syntax.json"></a>

```
{
  "[WhatIfPointScenario](#cfn-quicksight-dashboard-forecastscenario-whatifpointscenario)" : WhatIfPointScenario,
  "[WhatIfRangeScenario](#cfn-quicksight-dashboard-forecastscenario-whatifrangescenario)" : WhatIfRangeScenario
}
```

### YAML<a name="aws-properties-quicksight-dashboard-forecastscenario-syntax.yaml"></a>

```
  [WhatIfPointScenario](#cfn-quicksight-dashboard-forecastscenario-whatifpointscenario): 
    WhatIfPointScenario
  [WhatIfRangeScenario](#cfn-quicksight-dashboard-forecastscenario-whatifrangescenario): 
    WhatIfRangeScenario
```

## Properties<a name="aws-properties-quicksight-dashboard-forecastscenario-properties"></a>

`WhatIfPointScenario`  <a name="cfn-quicksight-dashboard-forecastscenario-whatifpointscenario"></a>
The what\-if analysis forecast setup with the target date\.  
*Required*: No  
*Type*: [WhatIfPointScenario](aws-properties-quicksight-dashboard-whatifpointscenario.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WhatIfRangeScenario`  <a name="cfn-quicksight-dashboard-forecastscenario-whatifrangescenario"></a>
The what\-if analysis forecast setup with the date range\.  
*Required*: No  
*Type*: [WhatIfRangeScenario](aws-properties-quicksight-dashboard-whatifrangescenario.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)