# Amazon CloudWatch Events Rule InputTransformer<a name="aws-properties-events-rule-inputtransformer"></a>

<a name="aws-properties-events-rule-inputtransformer-description"></a>The `InputTransformer` property type specifies settings that provide custom input to an Amazon CloudWatch Events rule target based on certain event data\.

<a name="aws-properties-events-rule-inputtransformer-inheritance"></a> `InputTransformer` is a property of the [CloudWatch Events Rule Target](aws-properties-events-rule-target.md) property type\. 

## Syntax<a name="aws-properties-events-rule-inputtransformer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-inputtransformer-syntax.json"></a>

```
{
  "[InputPathsMap](#cfn-events-rule-inputtransformer-inputpathsmap)" : { String:String, ... },
  "[InputTemplate](#cfn-events-rule-inputtransformer-inputtemplate)" : String
}
```

### YAML<a name="aws-properties-events-rule-inputtransformer-syntax.yaml"></a>

```
[InputPathsMap](#cfn-events-rule-inputtransformer-inputpathsmap): 
  String: String
[InputTemplate](#cfn-events-rule-inputtransformer-inputtemplate): String
```

## Properties<a name="aws-properties-events-rule-inputtransformer-properties"></a>

For more information, including constraints, see [InputTransformer](http://docs.aws.amazon.com/AmazonCloudWatchEvents/latest/APIReference/API_InputTransformer.html) in the *Amazon CloudWatch Events API Reference*\.

`InputPathsMap`  <a name="cfn-events-rule-inputtransformer-inputpathsmap"></a>
The map of JSON paths to extract from the event, as key\-value pairs where each value is a JSON path\. You must use JSON dot notation, not bracket notation\. Duplicates aren't allowed\.  
 *Required*: No  
 *Type*: String\-to\-string map  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InputTemplate`  <a name="cfn-events-rule-inputtransformer-inputtemplate"></a>
The input template where you can use the values of the keys from `InputPathsMap` to customize the data that's sent to the target\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 