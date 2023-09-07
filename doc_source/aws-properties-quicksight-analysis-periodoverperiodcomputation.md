# AWS::QuickSight::Analysis PeriodOverPeriodComputation<a name="aws-properties-quicksight-analysis-periodoverperiodcomputation"></a>

The period over period computation configuration\.

## Syntax<a name="aws-properties-quicksight-analysis-periodoverperiodcomputation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-periodoverperiodcomputation-syntax.json"></a>

```
{
  "[ComputationId](#cfn-quicksight-analysis-periodoverperiodcomputation-computationid)" : String,
  "[Name](#cfn-quicksight-analysis-periodoverperiodcomputation-name)" : String,
  "[Time](#cfn-quicksight-analysis-periodoverperiodcomputation-time)" : DimensionField,
  "[Value](#cfn-quicksight-analysis-periodoverperiodcomputation-value)" : MeasureField
}
```

### YAML<a name="aws-properties-quicksight-analysis-periodoverperiodcomputation-syntax.yaml"></a>

```
  [ComputationId](#cfn-quicksight-analysis-periodoverperiodcomputation-computationid): String
  [Name](#cfn-quicksight-analysis-periodoverperiodcomputation-name): String
  [Time](#cfn-quicksight-analysis-periodoverperiodcomputation-time): 
    DimensionField
  [Value](#cfn-quicksight-analysis-periodoverperiodcomputation-value): 
    MeasureField
```

## Properties<a name="aws-properties-quicksight-analysis-periodoverperiodcomputation-properties"></a>

`ComputationId`  <a name="cfn-quicksight-analysis-periodoverperiodcomputation-computationid"></a>
The ID for a computation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-analysis-periodoverperiodcomputation-name"></a>
The name of a computation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Time`  <a name="cfn-quicksight-analysis-periodoverperiodcomputation-time"></a>
The time field that is used in a computation\.  
*Required*: No  
*Type*: [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-analysis-periodoverperiodcomputation-value"></a>
The value field that is used in a computation\.  
*Required*: No  
*Type*: [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)