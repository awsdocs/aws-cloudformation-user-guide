# AWS::QuickSight::Template PeriodToDateComputation<a name="aws-properties-quicksight-template-periodtodatecomputation"></a>

The period to date computation configuration\.

## Syntax<a name="aws-properties-quicksight-template-periodtodatecomputation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-periodtodatecomputation-syntax.json"></a>

```
{
  "[ComputationId](#cfn-quicksight-template-periodtodatecomputation-computationid)" : String,
  "[Name](#cfn-quicksight-template-periodtodatecomputation-name)" : String,
  "[PeriodTimeGranularity](#cfn-quicksight-template-periodtodatecomputation-periodtimegranularity)" : String,
  "[Time](#cfn-quicksight-template-periodtodatecomputation-time)" : DimensionField,
  "[Value](#cfn-quicksight-template-periodtodatecomputation-value)" : MeasureField
}
```

### YAML<a name="aws-properties-quicksight-template-periodtodatecomputation-syntax.yaml"></a>

```
  [ComputationId](#cfn-quicksight-template-periodtodatecomputation-computationid): String
  [Name](#cfn-quicksight-template-periodtodatecomputation-name): String
  [PeriodTimeGranularity](#cfn-quicksight-template-periodtodatecomputation-periodtimegranularity): String
  [Time](#cfn-quicksight-template-periodtodatecomputation-time): 
    DimensionField
  [Value](#cfn-quicksight-template-periodtodatecomputation-value): 
    MeasureField
```

## Properties<a name="aws-properties-quicksight-template-periodtodatecomputation-properties"></a>

`ComputationId`  <a name="cfn-quicksight-template-periodtodatecomputation-computationid"></a>
The ID for a computation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-template-periodtodatecomputation-name"></a>
The name of a computation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PeriodTimeGranularity`  <a name="cfn-quicksight-template-periodtodatecomputation-periodtimegranularity"></a>
The time granularity setup of period to date computation\. Choose from the following options:  
+ YEAR: Year to date\.
+ MONTH: Month to date\.
*Required*: No  
*Type*: String  
*Allowed values*: `DAY | HOUR | MILLISECOND | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Time`  <a name="cfn-quicksight-template-periodtodatecomputation-time"></a>
The time field that is used in a computation\.  
*Required*: No  
*Type*: [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-template-periodtodatecomputation-value"></a>
The value field that is used in a computation\.  
*Required*: No  
*Type*: [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)