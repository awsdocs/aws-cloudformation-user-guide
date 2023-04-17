# AWS::QuickSight::Template MeasureField<a name="aws-properties-quicksight-template-measurefield"></a>

The measure \(metric\) type field\.

## Syntax<a name="aws-properties-quicksight-template-measurefield-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-measurefield-syntax.json"></a>

```
{
  "[CalculatedMeasureField](#cfn-quicksight-template-measurefield-calculatedmeasurefield)" : CalculatedMeasureField,
  "[CategoricalMeasureField](#cfn-quicksight-template-measurefield-categoricalmeasurefield)" : CategoricalMeasureField,
  "[DateMeasureField](#cfn-quicksight-template-measurefield-datemeasurefield)" : DateMeasureField,
  "[NumericalMeasureField](#cfn-quicksight-template-measurefield-numericalmeasurefield)" : NumericalMeasureField
}
```

### YAML<a name="aws-properties-quicksight-template-measurefield-syntax.yaml"></a>

```
  [CalculatedMeasureField](#cfn-quicksight-template-measurefield-calculatedmeasurefield): 
    CalculatedMeasureField
  [CategoricalMeasureField](#cfn-quicksight-template-measurefield-categoricalmeasurefield): 
    CategoricalMeasureField
  [DateMeasureField](#cfn-quicksight-template-measurefield-datemeasurefield): 
    DateMeasureField
  [NumericalMeasureField](#cfn-quicksight-template-measurefield-numericalmeasurefield): 
    NumericalMeasureField
```

## Properties<a name="aws-properties-quicksight-template-measurefield-properties"></a>

`CalculatedMeasureField`  <a name="cfn-quicksight-template-measurefield-calculatedmeasurefield"></a>
The calculated measure field only used in pivot tables\.  
*Required*: No  
*Type*: [CalculatedMeasureField](aws-properties-quicksight-template-calculatedmeasurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoricalMeasureField`  <a name="cfn-quicksight-template-measurefield-categoricalmeasurefield"></a>
The measure type field with categorical type columns\.  
*Required*: No  
*Type*: [CategoricalMeasureField](aws-properties-quicksight-template-categoricalmeasurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DateMeasureField`  <a name="cfn-quicksight-template-measurefield-datemeasurefield"></a>
The measure type field with date type columns\.  
*Required*: No  
*Type*: [DateMeasureField](aws-properties-quicksight-template-datemeasurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumericalMeasureField`  <a name="cfn-quicksight-template-measurefield-numericalmeasurefield"></a>
The measure type field with numerical type columns\.  
*Required*: No  
*Type*: [NumericalMeasureField](aws-properties-quicksight-template-numericalmeasurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)