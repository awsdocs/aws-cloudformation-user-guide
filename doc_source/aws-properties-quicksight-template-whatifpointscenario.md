# AWS::QuickSight::Template WhatIfPointScenario<a name="aws-properties-quicksight-template-whatifpointscenario"></a>

Provides the forecast to meet the target for a particular date\.

## Syntax<a name="aws-properties-quicksight-template-whatifpointscenario-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-whatifpointscenario-syntax.json"></a>

```
{
  "[Date](#cfn-quicksight-template-whatifpointscenario-date)" : String,
  "[Value](#cfn-quicksight-template-whatifpointscenario-value)" : Double
}
```

### YAML<a name="aws-properties-quicksight-template-whatifpointscenario-syntax.yaml"></a>

```
  [Date](#cfn-quicksight-template-whatifpointscenario-date): String
  [Value](#cfn-quicksight-template-whatifpointscenario-value): Double
```

## Properties<a name="aws-properties-quicksight-template-whatifpointscenario-properties"></a>

`Date`  <a name="cfn-quicksight-template-whatifpointscenario-date"></a>
The date that you need the forecast results for\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-template-whatifpointscenario-value"></a>
The target value that you want to meet for the provided date\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)