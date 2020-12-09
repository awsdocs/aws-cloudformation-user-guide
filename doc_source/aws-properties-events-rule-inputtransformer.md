# AWS::Events::Rule InputTransformer<a name="aws-properties-events-rule-inputtransformer"></a>

The `InputTransformer` property type specifies settings that provide custom input to an EventBridge target based on certain event data\.

 `InputTransformer` is a property of the [Target](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-target.html) property type\.

## Syntax<a name="aws-properties-events-rule-inputtransformer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-inputtransformer-syntax.json"></a>

```
{
  "[InputPathsMap](#cfn-events-rule-inputtransformer-inputpathsmap)" : {Key : Value, ...},
  "[InputTemplate](#cfn-events-rule-inputtransformer-inputtemplate)" : String
}
```

### YAML<a name="aws-properties-events-rule-inputtransformer-syntax.yaml"></a>

```
  [InputPathsMap](#cfn-events-rule-inputtransformer-inputpathsmap): 
    Key : Value
  [InputTemplate](#cfn-events-rule-inputtransformer-inputtemplate): String
```

## Properties<a name="aws-properties-events-rule-inputtransformer-properties"></a>

`InputPathsMap`  <a name="cfn-events-rule-inputtransformer-inputpathsmap"></a>
Map of JSON paths to be extracted from the event\. You can then insert these in the template in `InputTemplate` to produce the output you want to be sent to the target\.  
 `InputPathsMap` is an array key\-value pairs, where each value is a valid JSON path\. You can have as many as 10 key\-value pairs\. You must use JSON dot notation, not bracket notation\.  
The keys cannot start with "AWS\."   
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputTemplate`  <a name="cfn-events-rule-inputtransformer-inputtemplate"></a>
Input template where you specify placeholders that will be filled with the values of the keys from `InputPathsMap` to customize the data sent to the target\. Enclose each `InputPathsMaps` value in brackets: <*value*> The `InputTemplate` must be valid JSON\. For more information, see [InputTransformer](https://docs.aws.amazon.com/eventbridge/latest/APIReference/API_InputTransformer.html#API_InputTransformer_Contents) in the *Amazon EventBridge API Reference*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `8192`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)