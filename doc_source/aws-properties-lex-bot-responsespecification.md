# AWS::Lex::Bot ResponseSpecification<a name="aws-properties-lex-bot-responsespecification"></a>

Specifies a list of message groups that Amazon Lex uses to respond the user input\.

## Syntax<a name="aws-properties-lex-bot-responsespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-responsespecification-syntax.json"></a>

```
{
  "[AllowInterrupt](#cfn-lex-bot-responsespecification-allowinterrupt)" : Boolean,
  "[MessageGroupsList](#cfn-lex-bot-responsespecification-messagegroupslist)" : [ MessageGroup, ... ]
}
```

### YAML<a name="aws-properties-lex-bot-responsespecification-syntax.yaml"></a>

```
  [AllowInterrupt](#cfn-lex-bot-responsespecification-allowinterrupt): Boolean
  [MessageGroupsList](#cfn-lex-bot-responsespecification-messagegroupslist): 
    - MessageGroup
```

## Properties<a name="aws-properties-lex-bot-responsespecification-properties"></a>

`AllowInterrupt`  <a name="cfn-lex-bot-responsespecification-allowinterrupt"></a>
Indicates whether the user can interrupt a speech response from Amazon Lex\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageGroupsList`  <a name="cfn-lex-bot-responsespecification-messagegroupslist"></a>
A collection of responses that Amazon Lex can send to the user\. Amazon Lex chooses the actual response to send at runtime\.  
*Required*: Yes  
*Type*: List of [MessageGroup](aws-properties-lex-bot-messagegroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)