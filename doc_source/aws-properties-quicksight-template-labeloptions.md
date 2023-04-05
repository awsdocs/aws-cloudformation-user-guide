# AWS::QuickSight::Template LabelOptions<a name="aws-properties-quicksight-template-labeloptions"></a>

The share label options for the labels\.

## Syntax<a name="aws-properties-quicksight-template-labeloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-labeloptions-syntax.json"></a>

```
{
  "[CustomLabel](#cfn-quicksight-template-labeloptions-customlabel)" : String,
  "[FontConfiguration](#cfn-quicksight-template-labeloptions-fontconfiguration)" : FontConfiguration,
  "[Visibility](#cfn-quicksight-template-labeloptions-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-labeloptions-syntax.yaml"></a>

```
  [CustomLabel](#cfn-quicksight-template-labeloptions-customlabel): String
  [FontConfiguration](#cfn-quicksight-template-labeloptions-fontconfiguration): 
    FontConfiguration
  [Visibility](#cfn-quicksight-template-labeloptions-visibility): String
```

## Properties<a name="aws-properties-quicksight-template-labeloptions-properties"></a>

`CustomLabel`  <a name="cfn-quicksight-template-labeloptions-customlabel"></a>
The text for the label\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontConfiguration`  <a name="cfn-quicksight-template-labeloptions-fontconfiguration"></a>
The font configuration of the label\.  
*Required*: No  
*Type*: [FontConfiguration](aws-properties-quicksight-template-fontconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-template-labeloptions-visibility"></a>
Determines whether or not the label is visible\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)