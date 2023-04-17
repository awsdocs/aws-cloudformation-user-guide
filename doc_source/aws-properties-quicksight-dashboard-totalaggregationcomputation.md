# AWS::QuickSight::Dashboard TotalAggregationComputation<a name="aws-properties-quicksight-dashboard-totalaggregationcomputation"></a>

The total aggregation computation configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-totalaggregationcomputation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-totalaggregationcomputation-syntax.json"></a>

```
{
  "[ComputationId](#cfn-quicksight-dashboard-totalaggregationcomputation-computationid)" : String,
  "[Name](#cfn-quicksight-dashboard-totalaggregationcomputation-name)" : String,
  "[Value](#cfn-quicksight-dashboard-totalaggregationcomputation-value)" : MeasureField
}
```

### YAML<a name="aws-properties-quicksight-dashboard-totalaggregationcomputation-syntax.yaml"></a>

```
  [ComputationId](#cfn-quicksight-dashboard-totalaggregationcomputation-computationid): String
  [Name](#cfn-quicksight-dashboard-totalaggregationcomputation-name): String
  [Value](#cfn-quicksight-dashboard-totalaggregationcomputation-value): 
    MeasureField
```

## Properties<a name="aws-properties-quicksight-dashboard-totalaggregationcomputation-properties"></a>

`ComputationId`  <a name="cfn-quicksight-dashboard-totalaggregationcomputation-computationid"></a>
The ID for a computation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-dashboard-totalaggregationcomputation-name"></a>
The name of a computation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-dashboard-totalaggregationcomputation-value"></a>
The value field that is used in a computation\.  
*Required*: Yes  
*Type*: [MeasureField](aws-properties-quicksight-dashboard-measurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)