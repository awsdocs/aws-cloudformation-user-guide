# AWS::StepFunctions::StateMachine TagsEntry<a name="aws-properties-stepfunctions-statemachine-tagsentry"></a>

The `TagsEntry` property specifies *tags* to identify a state machine\.

## Syntax<a name="aws-properties-stepfunctions-statemachine-tagsentry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-stepfunctions-statemachine-tagsentry-syntax.json"></a>

```
{
  "[Key](#cfn-stepfunctions-statemachine-tagsentry-key)" : String,
  "[Value](#cfn-stepfunctions-statemachine-tagsentry-value)" : String
}
```

### YAML<a name="aws-properties-stepfunctions-statemachine-tagsentry-syntax.yaml"></a>

```
  [Key](#cfn-stepfunctions-statemachine-tagsentry-key): String
  [Value](#cfn-stepfunctions-statemachine-tagsentry-value): String
```

## Properties<a name="aws-properties-stepfunctions-statemachine-tagsentry-properties"></a>

`Key`  <a name="cfn-stepfunctions-statemachine-tagsentry-key"></a>
The `key` for a key\-value pair in a tag entry\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-stepfunctions-statemachine-tagsentry-value"></a>
The `value` for a key\-value pair in a tag entry\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)