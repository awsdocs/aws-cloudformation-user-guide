# AWS::Lex::Bot SlotTypeValue<a name="aws-properties-lex-bot-slottypevalue"></a>

Each slot type can have a set of values\. Each `SlotTypeValue` represents a value that the slot type can take\.

## Syntax<a name="aws-properties-lex-bot-slottypevalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-slottypevalue-syntax.json"></a>

```
{
  "[SampleValue](#cfn-lex-bot-slottypevalue-samplevalue)" : SampleValue,
  "[Synonyms](#cfn-lex-bot-slottypevalue-synonyms)" : [ SampleValue, ... ]
}
```

### YAML<a name="aws-properties-lex-bot-slottypevalue-syntax.yaml"></a>

```
  [SampleValue](#cfn-lex-bot-slottypevalue-samplevalue): 
    SampleValue
  [Synonyms](#cfn-lex-bot-slottypevalue-synonyms): 
    - SampleValue
```

## Properties<a name="aws-properties-lex-bot-slottypevalue-properties"></a>

`SampleValue`  <a name="cfn-lex-bot-slottypevalue-samplevalue"></a>
The value of the slot type entry\.  
*Required*: Yes  
*Type*: [SampleValue](aws-properties-lex-bot-samplevalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Synonyms`  <a name="cfn-lex-bot-slottypevalue-synonyms"></a>
Additional values related to the slot type entry\.  
*Required*: No  
*Type*: List of [SampleValue](aws-properties-lex-bot-samplevalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)