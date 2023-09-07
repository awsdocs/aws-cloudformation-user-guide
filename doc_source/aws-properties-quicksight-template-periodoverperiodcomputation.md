# AWS::QuickSight::Template PeriodOverPeriodComputation<a name="aws-properties-quicksight-template-periodoverperiodcomputation"></a>

The period over period computation configuration\.

## Syntax<a name="aws-properties-quicksight-template-periodoverperiodcomputation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-periodoverperiodcomputation-syntax.json"></a>

```
{
  "[ComputationId](#cfn-quicksight-template-periodoverperiodcomputation-computationid)" : String,
  "[Name](#cfn-quicksight-template-periodoverperiodcomputation-name)" : String,
  "[Time](#cfn-quicksight-template-periodoverperiodcomputation-time)" : DimensionField,
  "[Value](#cfn-quicksight-template-periodoverperiodcomputation-value)" : MeasureField
}
```

### YAML<a name="aws-properties-quicksight-template-periodoverperiodcomputation-syntax.yaml"></a>

```
  [ComputationId](#cfn-quicksight-template-periodoverperiodcomputation-computationid): String
  [Name](#cfn-quicksight-template-periodoverperiodcomputation-name): String
  [Time](#cfn-quicksight-template-periodoverperiodcomputation-time): 
    DimensionField
  [Value](#cfn-quicksight-template-periodoverperiodcomputation-value): 
    MeasureField
```

## Properties<a name="aws-properties-quicksight-template-periodoverperiodcomputation-properties"></a>

`ComputationId`  <a name="cfn-quicksight-template-periodoverperiodcomputation-computationid"></a>
The ID for a computation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-template-periodoverperiodcomputation-name"></a>
The name of a computation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Time`  <a name="cfn-quicksight-template-periodoverperiodcomputation-time"></a>
The time field that is used in a computation\.  
*Required*: No  
*Type*: [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-template-periodoverperiodcomputation-value"></a>
The value field that is used in a computation\.  
*Required*: No  
*Type*: [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)