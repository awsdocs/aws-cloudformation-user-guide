# AWS::QuickSight::Dashboard WhatIfRangeScenario<a name="aws-properties-quicksight-dashboard-whatifrangescenario"></a>

Provides the forecast to meet the target for a particular date range\.

## Syntax<a name="aws-properties-quicksight-dashboard-whatifrangescenario-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-whatifrangescenario-syntax.json"></a>

```
{
  "[EndDate](#cfn-quicksight-dashboard-whatifrangescenario-enddate)" : String,
  "[StartDate](#cfn-quicksight-dashboard-whatifrangescenario-startdate)" : String,
  "[Value](#cfn-quicksight-dashboard-whatifrangescenario-value)" : Double
}
```

### YAML<a name="aws-properties-quicksight-dashboard-whatifrangescenario-syntax.yaml"></a>

```
  [EndDate](#cfn-quicksight-dashboard-whatifrangescenario-enddate): String
  [StartDate](#cfn-quicksight-dashboard-whatifrangescenario-startdate): String
  [Value](#cfn-quicksight-dashboard-whatifrangescenario-value): Double
```

## Properties<a name="aws-properties-quicksight-dashboard-whatifrangescenario-properties"></a>

`EndDate`  <a name="cfn-quicksight-dashboard-whatifrangescenario-enddate"></a>
The end date in the date range that you need the forecast results for\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartDate`  <a name="cfn-quicksight-dashboard-whatifrangescenario-startdate"></a>
The start date in the date range that you need the forecast results for\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-dashboard-whatifrangescenario-value"></a>
The target value that you want to meet for the provided date range\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)