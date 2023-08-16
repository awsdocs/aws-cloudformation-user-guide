# AWS::WAFv2::LoggingConfiguration Condition<a name="aws-properties-wafv2-loggingconfiguration-condition"></a>

A single match condition for a log filter\.

## Syntax<a name="aws-properties-wafv2-loggingconfiguration-condition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-loggingconfiguration-condition-syntax.json"></a>

```
{
  "[ActionCondition](#cfn-wafv2-loggingconfiguration-condition-actioncondition)" : ActionCondition,
  "[LabelNameCondition](#cfn-wafv2-loggingconfiguration-condition-labelnamecondition)" : LabelNameCondition
}
```

### YAML<a name="aws-properties-wafv2-loggingconfiguration-condition-syntax.yaml"></a>

```
  [ActionCondition](#cfn-wafv2-loggingconfiguration-condition-actioncondition): 
    ActionCondition
  [LabelNameCondition](#cfn-wafv2-loggingconfiguration-condition-labelnamecondition): 
    LabelNameCondition
```

## Properties<a name="aws-properties-wafv2-loggingconfiguration-condition-properties"></a>

`ActionCondition`  <a name="cfn-wafv2-loggingconfiguration-condition-actioncondition"></a>
A single action condition\. This is the action setting that a log record must contain in order to meet the condition\.  
*Required*: No  
*Type*: [ActionCondition](aws-properties-wafv2-loggingconfiguration-actioncondition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LabelNameCondition`  <a name="cfn-wafv2-loggingconfiguration-condition-labelnamecondition"></a>
A single label name condition\. This is the fully qualified label name that a log record must contain in order to meet the condition\. Fully qualified labels have a prefix, optional namespaces, and label name\. The prefix identifies the rule group or web ACL context of the rule that added the label\.   
*Required*: No  
*Type*: [LabelNameCondition](aws-properties-wafv2-loggingconfiguration-labelnamecondition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)