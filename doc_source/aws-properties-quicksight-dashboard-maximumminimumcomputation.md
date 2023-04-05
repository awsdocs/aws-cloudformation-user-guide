# AWS::QuickSight::Dashboard MaximumMinimumComputation<a name="aws-properties-quicksight-dashboard-maximumminimumcomputation"></a>

The maximum and minimum computation configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-maximumminimumcomputation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-maximumminimumcomputation-syntax.json"></a>

```
{
  "[ComputationId](#cfn-quicksight-dashboard-maximumminimumcomputation-computationid)" : String,
  "[Name](#cfn-quicksight-dashboard-maximumminimumcomputation-name)" : String,
  "[Time](#cfn-quicksight-dashboard-maximumminimumcomputation-time)" : DimensionField,
  "[Type](#cfn-quicksight-dashboard-maximumminimumcomputation-type)" : String,
  "[Value](#cfn-quicksight-dashboard-maximumminimumcomputation-value)" : MeasureField
}
```

### YAML<a name="aws-properties-quicksight-dashboard-maximumminimumcomputation-syntax.yaml"></a>

```
  [ComputationId](#cfn-quicksight-dashboard-maximumminimumcomputation-computationid): String
  [Name](#cfn-quicksight-dashboard-maximumminimumcomputation-name): String
  [Time](#cfn-quicksight-dashboard-maximumminimumcomputation-time): 
    DimensionField
  [Type](#cfn-quicksight-dashboard-maximumminimumcomputation-type): String
  [Value](#cfn-quicksight-dashboard-maximumminimumcomputation-value): 
    MeasureField
```

## Properties<a name="aws-properties-quicksight-dashboard-maximumminimumcomputation-properties"></a>

`ComputationId`  <a name="cfn-quicksight-dashboard-maximumminimumcomputation-computationid"></a>
The ID for a computation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-dashboard-maximumminimumcomputation-name"></a>
The name of a computation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Time`  <a name="cfn-quicksight-dashboard-maximumminimumcomputation-time"></a>
The time field that is used in a computation\.  
*Required*: Yes  
*Type*: [DimensionField](aws-properties-quicksight-dashboard-dimensionfield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-dashboard-maximumminimumcomputation-type"></a>
The type of computation\. Choose one of the following options:  
+ MAXIMUM: A maximum computation\.
+ MINIMUM: A minimum computation\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `MAXIMUM | MINIMUM`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-dashboard-maximumminimumcomputation-value"></a>
The value field that is used in a computation\.  
*Required*: No  
*Type*: [MeasureField](aws-properties-quicksight-dashboard-measurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)