# AWS::Lex::Bot SlotDefaultValueSpecification<a name="aws-properties-lex-bot-slotdefaultvaluespecification"></a>

The default value to use when a user doesn't provide a value for a slot\.

## Syntax<a name="aws-properties-lex-bot-slotdefaultvaluespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-slotdefaultvaluespecification-syntax.json"></a>

```
{
  "[DefaultValueList](#cfn-lex-bot-slotdefaultvaluespecification-defaultvaluelist)" : [ SlotDefaultValue, ... ]
}
```

### YAML<a name="aws-properties-lex-bot-slotdefaultvaluespecification-syntax.yaml"></a>

```
  [DefaultValueList](#cfn-lex-bot-slotdefaultvaluespecification-defaultvaluelist): 
    - SlotDefaultValue
```

## Properties<a name="aws-properties-lex-bot-slotdefaultvaluespecification-properties"></a>

`DefaultValueList`  <a name="cfn-lex-bot-slotdefaultvaluespecification-defaultvaluelist"></a>
A list of default values\. Amazon Lex chooses the default value to use in the order that they are presented in the list\.  
*Required*: Yes  
*Type*: List of [SlotDefaultValue](aws-properties-lex-bot-slotdefaultvalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)