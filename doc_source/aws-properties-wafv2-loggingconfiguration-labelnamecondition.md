# AWS::WAFv2::LoggingConfiguration LabelNameCondition<a name="aws-properties-wafv2-loggingconfiguration-labelnamecondition"></a>

A single label name condition for a condition in a logging filter\.

## Syntax<a name="aws-properties-wafv2-loggingconfiguration-labelnamecondition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-loggingconfiguration-labelnamecondition-syntax.json"></a>

```
{
  "[LabelName](#cfn-wafv2-loggingconfiguration-labelnamecondition-labelname)" : String
}
```

### YAML<a name="aws-properties-wafv2-loggingconfiguration-labelnamecondition-syntax.yaml"></a>

```
  [LabelName](#cfn-wafv2-loggingconfiguration-labelnamecondition-labelname): String
```

## Properties<a name="aws-properties-wafv2-loggingconfiguration-labelnamecondition-properties"></a>

`LabelName`  <a name="cfn-wafv2-loggingconfiguration-labelnamecondition-labelname"></a>
The label name that a log record must contain in order to meet the condition\. This must be a fully qualified label name\. Fully qualified labels have a prefix, optional namespaces, and label name\. The prefix identifies the rule group or web ACL context of the rule that added the label\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^[0-9A-Za-z_\-:]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)