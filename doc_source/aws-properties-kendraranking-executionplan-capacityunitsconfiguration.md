# AWS::KendraRanking::ExecutionPlan CapacityUnitsConfiguration<a name="aws-properties-kendraranking-executionplan-capacityunitsconfiguration"></a>

Sets additional capacity units configured for your rescore execution plan\. A rescore execution plan is an Amazon Kendra Intelligent Ranking resource used for provisioning the `Rescore` API\. You can add and remove capacity units to fit your usage requirements\.

## Syntax<a name="aws-properties-kendraranking-executionplan-capacityunitsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendraranking-executionplan-capacityunitsconfiguration-syntax.json"></a>

```
{
  "[RescoreCapacityUnits](#cfn-kendraranking-executionplan-capacityunitsconfiguration-rescorecapacityunits)" : Integer
}
```

### YAML<a name="aws-properties-kendraranking-executionplan-capacityunitsconfiguration-syntax.yaml"></a>

```
  [RescoreCapacityUnits](#cfn-kendraranking-executionplan-capacityunitsconfiguration-rescorecapacityunits): Integer
```

## Properties<a name="aws-properties-kendraranking-executionplan-capacityunitsconfiguration-properties"></a>

`RescoreCapacityUnits`  <a name="cfn-kendraranking-executionplan-capacityunitsconfiguration-rescorecapacityunits"></a>
The amount of extra capacity for your rescore execution plan\.  
A single extra capacity unit for a rescore execution plan provides 0\.01 rescore requests per second\. You can add up to 1000 extra capacity units\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)