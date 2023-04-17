# AWS::QuickSight::Template ConditionalFormattingIcon<a name="aws-properties-quicksight-template-conditionalformattingicon"></a>

The formatting configuration for the icon\.

## Syntax<a name="aws-properties-quicksight-template-conditionalformattingicon-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-conditionalformattingicon-syntax.json"></a>

```
{
  "[CustomCondition](#cfn-quicksight-template-conditionalformattingicon-customcondition)" : ConditionalFormattingCustomIconCondition,
  "[IconSet](#cfn-quicksight-template-conditionalformattingicon-iconset)" : ConditionalFormattingIconSet
}
```

### YAML<a name="aws-properties-quicksight-template-conditionalformattingicon-syntax.yaml"></a>

```
  [CustomCondition](#cfn-quicksight-template-conditionalformattingicon-customcondition): 
    ConditionalFormattingCustomIconCondition
  [IconSet](#cfn-quicksight-template-conditionalformattingicon-iconset): 
    ConditionalFormattingIconSet
```

## Properties<a name="aws-properties-quicksight-template-conditionalformattingicon-properties"></a>

`CustomCondition`  <a name="cfn-quicksight-template-conditionalformattingicon-customcondition"></a>
Determines the custom condition for an icon set\.  
*Required*: No  
*Type*: [ConditionalFormattingCustomIconCondition](aws-properties-quicksight-template-conditionalformattingcustomiconcondition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IconSet`  <a name="cfn-quicksight-template-conditionalformattingicon-iconset"></a>
Formatting configuration for icon set\.  
*Required*: No  
*Type*: [ConditionalFormattingIconSet](aws-properties-quicksight-template-conditionalformattingiconset.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)