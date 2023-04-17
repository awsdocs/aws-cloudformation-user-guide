# AWS::QuickSight::Analysis AxisDataOptions<a name="aws-properties-quicksight-analysis-axisdataoptions"></a>

The data options for an axis\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-axisdataoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-axisdataoptions-syntax.json"></a>

```
{
  "[DateAxisOptions](#cfn-quicksight-analysis-axisdataoptions-dateaxisoptions)" : DateAxisOptions,
  "[NumericAxisOptions](#cfn-quicksight-analysis-axisdataoptions-numericaxisoptions)" : NumericAxisOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-axisdataoptions-syntax.yaml"></a>

```
  [DateAxisOptions](#cfn-quicksight-analysis-axisdataoptions-dateaxisoptions): 
    DateAxisOptions
  [NumericAxisOptions](#cfn-quicksight-analysis-axisdataoptions-numericaxisoptions): 
    NumericAxisOptions
```

## Properties<a name="aws-properties-quicksight-analysis-axisdataoptions-properties"></a>

`DateAxisOptions`  <a name="cfn-quicksight-analysis-axisdataoptions-dateaxisoptions"></a>
The options for an axis with a date field\.  
*Required*: No  
*Type*: [DateAxisOptions](aws-properties-quicksight-analysis-dateaxisoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumericAxisOptions`  <a name="cfn-quicksight-analysis-axisdataoptions-numericaxisoptions"></a>
The options for an axis with a numeric field\.  
*Required*: No  
*Type*: [NumericAxisOptions](aws-properties-quicksight-analysis-numericaxisoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)