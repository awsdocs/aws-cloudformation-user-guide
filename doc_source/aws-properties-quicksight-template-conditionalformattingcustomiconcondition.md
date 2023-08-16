# AWS::QuickSight::Template ConditionalFormattingCustomIconCondition<a name="aws-properties-quicksight-template-conditionalformattingcustomiconcondition"></a>

Determines the custom condition for an icon set\.

## Syntax<a name="aws-properties-quicksight-template-conditionalformattingcustomiconcondition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-conditionalformattingcustomiconcondition-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-template-conditionalformattingcustomiconcondition-color)" : String,
  "[DisplayConfiguration](#cfn-quicksight-template-conditionalformattingcustomiconcondition-displayconfiguration)" : ConditionalFormattingIconDisplayConfiguration,
  "[Expression](#cfn-quicksight-template-conditionalformattingcustomiconcondition-expression)" : String,
  "[IconOptions](#cfn-quicksight-template-conditionalformattingcustomiconcondition-iconoptions)" : ConditionalFormattingCustomIconOptions
}
```

### YAML<a name="aws-properties-quicksight-template-conditionalformattingcustomiconcondition-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-template-conditionalformattingcustomiconcondition-color): String
  [DisplayConfiguration](#cfn-quicksight-template-conditionalformattingcustomiconcondition-displayconfiguration): 
    ConditionalFormattingIconDisplayConfiguration
  [Expression](#cfn-quicksight-template-conditionalformattingcustomiconcondition-expression): String
  [IconOptions](#cfn-quicksight-template-conditionalformattingcustomiconcondition-iconoptions): 
    ConditionalFormattingCustomIconOptions
```

## Properties<a name="aws-properties-quicksight-template-conditionalformattingcustomiconcondition-properties"></a>

`Color`  <a name="cfn-quicksight-template-conditionalformattingcustomiconcondition-color"></a>
Determines the color of the icon\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayConfiguration`  <a name="cfn-quicksight-template-conditionalformattingcustomiconcondition-displayconfiguration"></a>
Determines the icon display configuration\.  
*Required*: No  
*Type*: [ConditionalFormattingIconDisplayConfiguration](aws-properties-quicksight-template-conditionalformattingicondisplayconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expression`  <a name="cfn-quicksight-template-conditionalformattingcustomiconcondition-expression"></a>
The expression that determines the condition of the icon set\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IconOptions`  <a name="cfn-quicksight-template-conditionalformattingcustomiconcondition-iconoptions"></a>
Custom icon options for an icon set\.  
*Required*: Yes  
*Type*: [ConditionalFormattingCustomIconOptions](aws-properties-quicksight-template-conditionalformattingcustomiconoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)