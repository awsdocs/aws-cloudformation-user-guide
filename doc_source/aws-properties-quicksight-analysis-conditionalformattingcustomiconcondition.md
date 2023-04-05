# AWS::QuickSight::Analysis ConditionalFormattingCustomIconCondition<a name="aws-properties-quicksight-analysis-conditionalformattingcustomiconcondition"></a>

Determines the custom condition for an icon set\.

## Syntax<a name="aws-properties-quicksight-analysis-conditionalformattingcustomiconcondition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-conditionalformattingcustomiconcondition-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-analysis-conditionalformattingcustomiconcondition-color)" : String,
  "[DisplayConfiguration](#cfn-quicksight-analysis-conditionalformattingcustomiconcondition-displayconfiguration)" : ConditionalFormattingIconDisplayConfiguration,
  "[Expression](#cfn-quicksight-analysis-conditionalformattingcustomiconcondition-expression)" : String,
  "[IconOptions](#cfn-quicksight-analysis-conditionalformattingcustomiconcondition-iconoptions)" : ConditionalFormattingCustomIconOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-conditionalformattingcustomiconcondition-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-analysis-conditionalformattingcustomiconcondition-color): String
  [DisplayConfiguration](#cfn-quicksight-analysis-conditionalformattingcustomiconcondition-displayconfiguration): 
    ConditionalFormattingIconDisplayConfiguration
  [Expression](#cfn-quicksight-analysis-conditionalformattingcustomiconcondition-expression): String
  [IconOptions](#cfn-quicksight-analysis-conditionalformattingcustomiconcondition-iconoptions): 
    ConditionalFormattingCustomIconOptions
```

## Properties<a name="aws-properties-quicksight-analysis-conditionalformattingcustomiconcondition-properties"></a>

`Color`  <a name="cfn-quicksight-analysis-conditionalformattingcustomiconcondition-color"></a>
Determines the color of the icon\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayConfiguration`  <a name="cfn-quicksight-analysis-conditionalformattingcustomiconcondition-displayconfiguration"></a>
Determines the icon display configuration\.  
*Required*: No  
*Type*: [ConditionalFormattingIconDisplayConfiguration](aws-properties-quicksight-analysis-conditionalformattingicondisplayconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expression`  <a name="cfn-quicksight-analysis-conditionalformattingcustomiconcondition-expression"></a>
The expression that determines the condition of the icon set\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IconOptions`  <a name="cfn-quicksight-analysis-conditionalformattingcustomiconcondition-iconoptions"></a>
Custom icon options for an icon set\.  
*Required*: Yes  
*Type*: [ConditionalFormattingCustomIconOptions](aws-properties-quicksight-analysis-conditionalformattingcustomiconoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)