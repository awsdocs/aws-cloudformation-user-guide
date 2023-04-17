# AWS::QuickSight::Dashboard AxisLabelOptions<a name="aws-properties-quicksight-dashboard-axislabeloptions"></a>

The label options for a chart axis\. You must specify the field that the label is targeted to\.

## Syntax<a name="aws-properties-quicksight-dashboard-axislabeloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-axislabeloptions-syntax.json"></a>

```
{
  "[ApplyTo](#cfn-quicksight-dashboard-axislabeloptions-applyto)" : AxisLabelReferenceOptions,
  "[CustomLabel](#cfn-quicksight-dashboard-axislabeloptions-customlabel)" : String,
  "[FontConfiguration](#cfn-quicksight-dashboard-axislabeloptions-fontconfiguration)" : FontConfiguration
}
```

### YAML<a name="aws-properties-quicksight-dashboard-axislabeloptions-syntax.yaml"></a>

```
  [ApplyTo](#cfn-quicksight-dashboard-axislabeloptions-applyto): 
    AxisLabelReferenceOptions
  [CustomLabel](#cfn-quicksight-dashboard-axislabeloptions-customlabel): String
  [FontConfiguration](#cfn-quicksight-dashboard-axislabeloptions-fontconfiguration): 
    FontConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-axislabeloptions-properties"></a>

`ApplyTo`  <a name="cfn-quicksight-dashboard-axislabeloptions-applyto"></a>
The options that indicate which field the label belongs to\.  
*Required*: No  
*Type*: [AxisLabelReferenceOptions](aws-properties-quicksight-dashboard-axislabelreferenceoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomLabel`  <a name="cfn-quicksight-dashboard-axislabeloptions-customlabel"></a>
The text for the axis label\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontConfiguration`  <a name="cfn-quicksight-dashboard-axislabeloptions-fontconfiguration"></a>
The font configuration of the axis label\.  
*Required*: No  
*Type*: [FontConfiguration](aws-properties-quicksight-dashboard-fontconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)