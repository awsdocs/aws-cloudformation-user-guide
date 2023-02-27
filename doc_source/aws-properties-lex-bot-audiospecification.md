# AWS::Lex::Bot AudioSpecification<a name="aws-properties-lex-bot-audiospecification"></a>

Specifies the audio input specifications\.

## Syntax<a name="aws-properties-lex-bot-audiospecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-audiospecification-syntax.json"></a>

```
{
  "[EndTimeoutMs](#cfn-lex-bot-audiospecification-endtimeoutms)" : Integer,
  "[MaxLengthMs](#cfn-lex-bot-audiospecification-maxlengthms)" : Integer
}
```

### YAML<a name="aws-properties-lex-bot-audiospecification-syntax.yaml"></a>

```
  [EndTimeoutMs](#cfn-lex-bot-audiospecification-endtimeoutms): Integer
  [MaxLengthMs](#cfn-lex-bot-audiospecification-maxlengthms): Integer
```

## Properties<a name="aws-properties-lex-bot-audiospecification-properties"></a>

`EndTimeoutMs`  <a name="cfn-lex-bot-audiospecification-endtimeoutms"></a>
Time for which a bot waits after the customer stops speaking to assume the utterance is finished\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxLengthMs`  <a name="cfn-lex-bot-audiospecification-maxlengthms"></a>
Time for how long Amazon Lex waits before speech input is truncated and the speech is returned to application\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)