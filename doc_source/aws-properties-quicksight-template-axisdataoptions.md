# AWS::QuickSight::Template AxisDataOptions<a name="aws-properties-quicksight-template-axisdataoptions"></a>

The data options for an axis\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-axisdataoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-axisdataoptions-syntax.json"></a>

```
{
  "[DateAxisOptions](#cfn-quicksight-template-axisdataoptions-dateaxisoptions)" : DateAxisOptions,
  "[NumericAxisOptions](#cfn-quicksight-template-axisdataoptions-numericaxisoptions)" : NumericAxisOptions
}
```

### YAML<a name="aws-properties-quicksight-template-axisdataoptions-syntax.yaml"></a>

```
  [DateAxisOptions](#cfn-quicksight-template-axisdataoptions-dateaxisoptions): 
    DateAxisOptions
  [NumericAxisOptions](#cfn-quicksight-template-axisdataoptions-numericaxisoptions): 
    NumericAxisOptions
```

## Properties<a name="aws-properties-quicksight-template-axisdataoptions-properties"></a>

`DateAxisOptions`  <a name="cfn-quicksight-template-axisdataoptions-dateaxisoptions"></a>
The options for an axis with a date field\.  
*Required*: No  
*Type*: [DateAxisOptions](aws-properties-quicksight-template-dateaxisoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumericAxisOptions`  <a name="cfn-quicksight-template-axisdataoptions-numericaxisoptions"></a>
The options for an axis with a numeric field\.  
*Required*: No  
*Type*: [NumericAxisOptions](aws-properties-quicksight-template-numericaxisoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)