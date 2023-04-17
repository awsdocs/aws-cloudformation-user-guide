# AWS::QuickSight::Analysis AxisLabelOptions<a name="aws-properties-quicksight-analysis-axislabeloptions"></a>

The label options for a chart axis\. You must specify the field that the label is targeted to\.

## Syntax<a name="aws-properties-quicksight-analysis-axislabeloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-axislabeloptions-syntax.json"></a>

```
{
  "[ApplyTo](#cfn-quicksight-analysis-axislabeloptions-applyto)" : AxisLabelReferenceOptions,
  "[CustomLabel](#cfn-quicksight-analysis-axislabeloptions-customlabel)" : String,
  "[FontConfiguration](#cfn-quicksight-analysis-axislabeloptions-fontconfiguration)" : FontConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-axislabeloptions-syntax.yaml"></a>

```
  [ApplyTo](#cfn-quicksight-analysis-axislabeloptions-applyto): 
    AxisLabelReferenceOptions
  [CustomLabel](#cfn-quicksight-analysis-axislabeloptions-customlabel): String
  [FontConfiguration](#cfn-quicksight-analysis-axislabeloptions-fontconfiguration): 
    FontConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-axislabeloptions-properties"></a>

`ApplyTo`  <a name="cfn-quicksight-analysis-axislabeloptions-applyto"></a>
The options that indicate which field the label belongs to\.  
*Required*: No  
*Type*: [AxisLabelReferenceOptions](aws-properties-quicksight-analysis-axislabelreferenceoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomLabel`  <a name="cfn-quicksight-analysis-axislabeloptions-customlabel"></a>
The text for the axis label\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontConfiguration`  <a name="cfn-quicksight-analysis-axislabeloptions-fontconfiguration"></a>
The font configuration of the axis label\.  
*Required*: No  
*Type*: [FontConfiguration](aws-properties-quicksight-analysis-fontconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)