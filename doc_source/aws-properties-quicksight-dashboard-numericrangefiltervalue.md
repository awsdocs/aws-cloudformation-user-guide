# AWS::QuickSight::Dashboard NumericRangeFilterValue<a name="aws-properties-quicksight-dashboard-numericrangefiltervalue"></a>

The value input pf the numeric range filter\.

## Syntax<a name="aws-properties-quicksight-dashboard-numericrangefiltervalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-numericrangefiltervalue-syntax.json"></a>

```
{
  "[Parameter](#cfn-quicksight-dashboard-numericrangefiltervalue-parameter)" : String,
  "[StaticValue](#cfn-quicksight-dashboard-numericrangefiltervalue-staticvalue)" : Double
}
```

### YAML<a name="aws-properties-quicksight-dashboard-numericrangefiltervalue-syntax.yaml"></a>

```
  [Parameter](#cfn-quicksight-dashboard-numericrangefiltervalue-parameter): String
  [StaticValue](#cfn-quicksight-dashboard-numericrangefiltervalue-staticvalue): Double
```

## Properties<a name="aws-properties-quicksight-dashboard-numericrangefiltervalue-properties"></a>

`Parameter`  <a name="cfn-quicksight-dashboard-numericrangefiltervalue-parameter"></a>
The parameter that is used in the numeric range\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StaticValue`  <a name="cfn-quicksight-dashboard-numericrangefiltervalue-staticvalue"></a>
The static value of the numeric range filter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)